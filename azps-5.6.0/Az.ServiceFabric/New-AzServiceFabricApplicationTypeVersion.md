---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: d13e2e4473c390a27be4741de703818bda769efa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922298"
---
# <span data-ttu-id="b22de-101">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b22de-101">New-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="b22de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b22de-102">SYNOPSIS</span></span>
<span data-ttu-id="b22de-103">Új alkalmazástípus-verzió létrehozása a megadott erőforráscsoport és fürt alatt.</span><span class="sxs-lookup"><span data-stu-id="b22de-103">Create new application type version under the specified resource group and cluster.</span></span>

## <span data-ttu-id="b22de-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b22de-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> -PackageUrl <String> [-DefaultParameter <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b22de-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b22de-105">DESCRIPTION</span></span>
<span data-ttu-id="b22de-106">Ez a parancsmag új alkalmazástípus-verziót hoz létre a -PackageUrl fájlban megadott csomag használatával, ennek REST-végponton keresztül kell elérhetőnek lennie ahhoz, hogy az Azure Resource Manager felhasználja a telepítés során, és az .sfpkg kiterjesztéssel csomagolva és tömörítve tartalmazza az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="b22de-106">This cmdlet creates a new application type version using the package specified in -PackageUrl, this should be accessible through a REST endpoint for Azure Resource Manager to consume during deployment and contained The application packaged and zipped with the extension .sfpkg.</span></span> <span data-ttu-id="b22de-107">Ez a parancs létrehozza az alkalmazástípust, ha még nem létezik.</span><span class="sxs-lookup"><span data-stu-id="b22de-107">This command will create the application type if it doesn't exist already.</span></span>

## <span data-ttu-id="b22de-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b22de-108">EXAMPLES</span></span>

### <span data-ttu-id="b22de-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="b22de-109">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -PackageUrl $packageUrl -Verbose
```

<span data-ttu-id="b22de-110">Ebben a példában létrehozunk egy "v1" alkalmazástípusú verziót a "testAppType" típus alatt.</span><span class="sxs-lookup"><span data-stu-id="b22de-110">This example will create an application type version "v1" under type "testAppType".</span></span> <span data-ttu-id="b22de-111">Az alkalmazás jegyzékfájlban szereplő verziójának a -Version verzióban megadott verzióval kell azonosnak lennie.</span><span class="sxs-lookup"><span data-stu-id="b22de-111">The version in the application manifest contained in the package should have the same version as the one specified in -Version.</span></span>

## <span data-ttu-id="b22de-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b22de-112">PARAMETERS</span></span>

### <span data-ttu-id="b22de-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b22de-113">-ClusterName</span></span>
<span data-ttu-id="b22de-114">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="b22de-114">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b22de-115">-DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="b22de-115">-DefaultParameter</span></span>
<span data-ttu-id="b22de-116">Adja meg az alkalmazásparaméterek alapértelmezett értékeit kulcs-érték párokként.</span><span class="sxs-lookup"><span data-stu-id="b22de-116">Specify the default values of the application parameters as key/value pairs.</span></span>
<span data-ttu-id="b22de-117">Ezeknek a paramétereknek léteznie kell az alkalmazás jegyzékfájlban.</span><span class="sxs-lookup"><span data-stu-id="b22de-117">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b22de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b22de-118">-DefaultProfile</span></span>
<span data-ttu-id="b22de-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b22de-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22de-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b22de-120">-Force</span></span>
<span data-ttu-id="b22de-121">Folytatás kérések nélkül</span><span class="sxs-lookup"><span data-stu-id="b22de-121">Continue without prompts</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22de-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b22de-122">-Name</span></span>
<span data-ttu-id="b22de-123">Az alkalmazástípus nevének megadása</span><span class="sxs-lookup"><span data-stu-id="b22de-123">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22de-124">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="b22de-124">-PackageUrl</span></span>
<span data-ttu-id="b22de-125">Az alkalmazáscsomag sfpkg-fájl URL-címének megadása</span><span class="sxs-lookup"><span data-stu-id="b22de-125">Specify the url of the application package sfpkg file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b22de-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b22de-126">-ResourceGroupName</span></span>
<span data-ttu-id="b22de-127">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="b22de-127">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b22de-128">-Version</span><span class="sxs-lookup"><span data-stu-id="b22de-128">-Version</span></span>
<span data-ttu-id="b22de-129">Az alkalmazástípus verziójának megadása</span><span class="sxs-lookup"><span data-stu-id="b22de-129">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeVersion

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22de-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b22de-130">-Confirm</span></span>
<span data-ttu-id="b22de-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b22de-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22de-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b22de-132">-WhatIf</span></span>
<span data-ttu-id="b22de-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b22de-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b22de-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b22de-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22de-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b22de-135">CommonParameters</span></span>
<span data-ttu-id="b22de-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b22de-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b22de-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b22de-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b22de-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b22de-138">INPUTS</span></span>

### <span data-ttu-id="b22de-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b22de-139">System.String</span></span>

### <span data-ttu-id="b22de-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b22de-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b22de-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b22de-141">OUTPUTS</span></span>

### <span data-ttu-id="b22de-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b22de-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="b22de-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b22de-143">NOTES</span></span>

## <span data-ttu-id="b22de-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b22de-144">RELATED LINKS</span></span>
