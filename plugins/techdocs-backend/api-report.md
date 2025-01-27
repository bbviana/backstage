## API Report File for "@backstage/plugin-techdocs-backend"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
/// <reference types="node" />

import { CatalogApi } from '@backstage/catalog-client';
import { Config } from '@backstage/config';
import { DocumentCollatorFactory } from '@backstage/search-common';
import { Entity } from '@backstage/catalog-model';
import express from 'express';
import { GeneratorBuilder } from '@backstage/techdocs-common';
import { Knex } from 'knex';
import { Logger as Logger_2 } from 'winston';
import { Permission } from '@backstage/plugin-permission-common';
import { PluginCacheManager } from '@backstage/backend-common';
import { PluginEndpointDiscovery } from '@backstage/backend-common';
import { PreparerBuilder } from '@backstage/techdocs-common';
import { PublisherBase } from '@backstage/techdocs-common';
import { Readable } from 'stream';
import { TechDocsDocument } from '@backstage/techdocs-common';
import { TokenManager } from '@backstage/backend-common';

// @public
export function createRouter(options: RouterOptions): Promise<express.Router>;

// @public @deprecated
export class DefaultTechDocsCollator {
  // (undocumented)
  protected applyArgsToFormat(
    format: string,
    args: Record<string, string>,
  ): string;
  // (undocumented)
  execute(): Promise<TechDocsDocument[]>;
  // (undocumented)
  static fromConfig(
    config: Config,
    options: TechDocsCollatorOptions,
  ): DefaultTechDocsCollator;
  // (undocumented)
  readonly type: string;
  // (undocumented)
  readonly visibilityPermission: Permission;
}

// @public
export class DefaultTechDocsCollatorFactory implements DocumentCollatorFactory {
  // (undocumented)
  static fromConfig(
    config: Config,
    options: TechDocsCollatorFactoryOptions,
  ): DefaultTechDocsCollatorFactory;
  // (undocumented)
  getCollator(): Promise<Readable>;
  // (undocumented)
  readonly type: string;
  // (undocumented)
  readonly visibilityPermission: Permission;
}

// @public
export interface DocsBuildStrategy {
  // (undocumented)
  shouldBuild(params: ShouldBuildParameters): Promise<boolean>;
}

// @public
export type OutOfTheBoxDeploymentOptions = {
  preparers: PreparerBuilder;
  generators: GeneratorBuilder;
  publisher: PublisherBase;
  logger: Logger_2;
  discovery: PluginEndpointDiscovery;
  database?: Knex;
  config: Config;
  cache: PluginCacheManager;
  docsBuildStrategy?: DocsBuildStrategy;
};

// @public
export type RecommendedDeploymentOptions = {
  publisher: PublisherBase;
  logger: Logger_2;
  discovery: PluginEndpointDiscovery;
  config: Config;
  cache: PluginCacheManager;
  docsBuildStrategy?: DocsBuildStrategy;
};

// @public
export type RouterOptions =
  | RecommendedDeploymentOptions
  | OutOfTheBoxDeploymentOptions;

// @public
export type ShouldBuildParameters = {
  entity: Entity;
};

// @public
export type TechDocsCollatorFactoryOptions = {
  discovery: PluginEndpointDiscovery;
  logger: Logger_2;
  tokenManager: TokenManager;
  locationTemplate?: string;
  catalogClient?: CatalogApi;
  parallelismLimit?: number;
  legacyPathCasing?: boolean;
};

// @public
export type TechDocsCollatorOptions = {
  discovery: PluginEndpointDiscovery;
  logger: Logger_2;
  tokenManager: TokenManager;
  locationTemplate?: string;
  catalogClient?: CatalogApi;
  parallelismLimit?: number;
  legacyPathCasing?: boolean;
};

export { TechDocsDocument };

export * from '@backstage/techdocs-common';
```
