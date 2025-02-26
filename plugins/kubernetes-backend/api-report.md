## API Report File for "@backstage/plugin-kubernetes-backend"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
import { Config } from '@backstage/config';
import express from 'express';
import { FetchResponse } from '@backstage/plugin-kubernetes-common';
import { KubernetesFetchError } from '@backstage/plugin-kubernetes-common';
import { KubernetesRequestBody } from '@backstage/plugin-kubernetes-common';
import { Logger as Logger_2 } from 'winston';

// Warning: (ae-missing-release-tag) "ClusterDetails" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface ClusterDetails {
  // (undocumented)
  authProvider: string;
  // (undocumented)
  name: string;
  // (undocumented)
  serviceAccountToken?: string | undefined;
  // (undocumented)
  skipTLSVerify?: boolean;
  // (undocumented)
  url: string;
}

// Warning: (ae-missing-release-tag) "createRouter" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export function createRouter(options: RouterOptions): Promise<express.Router>;

// Warning: (ae-missing-release-tag) "CustomResource" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface CustomResource {
  // (undocumented)
  apiVersion: string;
  // (undocumented)
  group: string;
  // (undocumented)
  plural: string;
}

// Warning: (ae-missing-release-tag) "FetchResponseWrapper" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface FetchResponseWrapper {
  // (undocumented)
  errors: KubernetesFetchError[];
  // (undocumented)
  responses: FetchResponse[];
}

// Warning: (ae-missing-release-tag) "KubernetesClustersSupplier" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface KubernetesClustersSupplier {
  // (undocumented)
  getClusters(): Promise<ClusterDetails[]>;
}

// Warning: (ae-missing-release-tag) "KubernetesFetcher" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface KubernetesFetcher {
  // (undocumented)
  fetchObjectsForService(
    params: ObjectFetchParams,
  ): Promise<FetchResponseWrapper>;
}

// Warning: (ae-missing-release-tag) "KubernetesObjectTypes" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export type KubernetesObjectTypes =
  | 'pods'
  | 'services'
  | 'configmaps'
  | 'deployments'
  | 'replicasets'
  | 'horizontalpodautoscalers'
  | 'ingresses'
  | 'customresources';

// Warning: (ae-missing-release-tag) "KubernetesServiceLocator" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface KubernetesServiceLocator {
  // (undocumented)
  getClustersByServiceId(serviceId: string): Promise<ClusterDetails[]>;
}

// Warning: (ae-forgotten-export) The symbol "KubernetesFanOutHandler" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "makeRouter" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const makeRouter: (
  logger: Logger_2,
  kubernetesFanOutHandler: KubernetesFanOutHandler,
  clusterDetails: ClusterDetails[],
) => express.Router;

// Warning: (ae-missing-release-tag) "ObjectFetchParams" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface ObjectFetchParams {
  // (undocumented)
  clusterDetails: ClusterDetails;
  // (undocumented)
  customResources: CustomResource[];
  // (undocumented)
  labelSelector: string;
  // (undocumented)
  objectTypesToFetch: Set<KubernetesObjectTypes>;
  // (undocumented)
  serviceId: string;
}

// Warning: (ae-missing-release-tag) "RouterOptions" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface RouterOptions {
  // (undocumented)
  clusterSupplier?: KubernetesClustersSupplier;
  // (undocumented)
  config: Config;
  // (undocumented)
  logger: Logger_2;
}

// Warning: (ae-missing-release-tag) "ServiceLocatorMethod" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export type ServiceLocatorMethod = 'multiTenant' | 'http';

// (No @packageDocumentation comment for this package)
```
