## API Report File for "@backstage/plugin-tech-radar"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
/// <reference types="react" />

import { ApiRef } from '@backstage/core-plugin-api';
import { BackstagePlugin } from '@backstage/core-plugin-api';
import { RouteRef } from '@backstage/core-plugin-api';

// Warning: (ae-missing-release-tag) "RadarEntry" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface RadarEntry {
  // (undocumented)
  description?: string;
  // (undocumented)
  id: string;
  // (undocumented)
  key: string;
  // (undocumented)
  quadrant: string;
  // (undocumented)
  timeline: Array<RadarEntrySnapshot>;
  // (undocumented)
  title: string;
  // (undocumented)
  url: string;
}

// Warning: (ae-missing-release-tag) "RadarEntrySnapshot" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface RadarEntrySnapshot {
  // (undocumented)
  date: Date;
  // (undocumented)
  description?: string;
  // Warning: (ae-forgotten-export) The symbol "MovedState" needs to be exported by the entry point index.d.ts
  //
  // (undocumented)
  moved?: MovedState;
  // (undocumented)
  ringId: string;
}

// Warning: (ae-missing-release-tag) "RadarQuadrant" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface RadarQuadrant {
  // (undocumented)
  id: string;
  // (undocumented)
  name: string;
}

// Warning: (ae-missing-release-tag) "RadarRing" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface RadarRing {
  // (undocumented)
  color: string;
  // (undocumented)
  id: string;
  // (undocumented)
  name: string;
}

// Warning: (ae-missing-release-tag) "RadarPage" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const Router: {
  ({ title, subtitle, pageTitle, ...props }: TechRadarPageProps): JSX.Element;
  defaultProps: {
    title: string;
    subtitle: string;
    pageTitle: string;
  };
};

// Warning: (ae-missing-release-tag) "TechRadarApi" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface TechRadarApi {
  load: (id: string | undefined) => Promise<TechRadarLoaderResponse>;
}

// Warning: (ae-missing-release-tag) "techRadarApiRef" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const techRadarApiRef: ApiRef<TechRadarApi>;

// Warning: (ae-missing-release-tag) "RadarComponent" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const TechRadarComponent: (
  props: TechRadarComponentProps,
) => JSX.Element;

// Warning: (ae-missing-release-tag) "TechRadarComponentProps" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface TechRadarComponentProps {
  // (undocumented)
  height: number;
  // (undocumented)
  id?: string;
  // (undocumented)
  svgProps?: object;
  // (undocumented)
  width: number;
}

// Warning: (ae-missing-release-tag) "TechRadarLoaderResponse" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface TechRadarLoaderResponse {
  // (undocumented)
  entries: RadarEntry[];
  // (undocumented)
  quadrants: RadarQuadrant[];
  // (undocumented)
  rings: RadarRing[];
}

// Warning: (ae-missing-release-tag) "TechRadarPage" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const TechRadarPage: {
  ({ title, subtitle, pageTitle, ...props }: TechRadarPageProps): JSX.Element;
  defaultProps: {
    title: string;
    subtitle: string;
    pageTitle: string;
  };
};

// Warning: (ae-missing-release-tag) "techRadarPlugin" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
const techRadarPlugin: BackstagePlugin<
  {
    root: RouteRef<undefined>;
  },
  {}
>;
export { techRadarPlugin as plugin };
export { techRadarPlugin };

// Warnings were encountered during analysis:
//
// src/components/RadarPage.d.ts:9:5 - (ae-forgotten-export) The symbol "TechRadarPageProps" needs to be exported by the entry point index.d.ts
```