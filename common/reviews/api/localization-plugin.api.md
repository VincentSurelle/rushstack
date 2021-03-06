## API Report File for "@rushstack/localization-plugin"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { Terminal } from '@microsoft/node-core-library';
import * as Webpack from 'webpack';

// @public (undocumented)
export interface IDefaultLocaleOptions {
    // (undocumented)
    locale?: string;
    passthroughLocaleName?: string;
    // (undocumented)
    usePassthroughLocale?: boolean;
}

// @public (undocumented)
export interface ILocale {
    // (undocumented)
    [locFilePath: string]: ILocaleFileData;
}

// @public (undocumented)
export interface ILocaleFileData {
    // (undocumented)
    [stringName: string]: string;
}

// @public (undocumented)
export interface ILocales {
    // (undocumented)
    [locale: string]: ILocale;
}

// @public
export interface ILocalizationPluginOptions {
    // (undocumented)
    defaultLocale: IDefaultLocaleOptions;
    // (undocumented)
    exportAsDefault?: boolean;
    // (undocumented)
    filesToIgnore?: string[];
    // (undocumented)
    localizationStatsCallback?: (stats: ILocalizationStats) => void;
    // (undocumented)
    localizationStatsDropPath?: string;
    // (undocumented)
    localizedStrings: ILocales;
    // (undocumented)
    typingsOptions?: ITypingsGenerationOptions;
}

// @public (undocumented)
export interface ILocalizationStats {
    // (undocumented)
    entrypoints: {
        [name: string]: ILocalizationStatsEntrypoint;
    };
    // (undocumented)
    namedChunkGroups: {
        [name: string]: ILocalizationStatsChunkGroup;
    };
}

// @public (undocumented)
export interface ILocalizationStatsChunkGroup {
    // (undocumented)
    localizedAssets: {
        [locale: string]: string;
    };
}

// @public (undocumented)
export interface ILocalizationStatsEntrypoint {
    // (undocumented)
    localizedAssets: {
        [locale: string]: string;
    };
}

// @public (undocumented)
export interface ILocFilePreprocessorOptions {
    // (undocumented)
    exportAsDefault?: boolean;
    // (undocumented)
    filesToIgnore?: string[];
    // (undocumented)
    generatedTsFolder: string;
    // (undocumented)
    srcFolder: string;
    // (undocumented)
    terminal?: Terminal;
}

// @internal (undocumented)
export interface _IStringPlaceholder {
    // (undocumented)
    suffix: string;
    // (undocumented)
    value: string;
}

// @public (undocumented)
export interface ITypingsGenerationOptions {
    // (undocumented)
    generatedTsFolder: string;
    // (undocumented)
    sourceRoot?: string;
}

// @public
export class LocalizationPlugin implements Webpack.Plugin {
    constructor(options: ILocalizationPluginOptions);
    // (undocumented)
    apply(compiler: Webpack.Compiler): void;
    // @internal (undocumented)
    stringKeys: Map<string, _IStringPlaceholder>;
    }

// @public
export class LocFilePreprocessor {
    constructor(options: ILocFilePreprocessorOptions);
    // (undocumented)
    generateTypings(): void;
    // (undocumented)
    runWatcher(): void;
}


// (No @packageDocumentation comment for this package)

```
