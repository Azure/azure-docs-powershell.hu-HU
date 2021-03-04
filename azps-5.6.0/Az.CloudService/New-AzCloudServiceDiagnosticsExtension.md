---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/new-azcloudservicediagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
ms.openlocfilehash: a87e9c76b2c083392fc37d74a3ba213dba5881ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927418"
---
# <span data-ttu-id="04a96-101">New-AzCloudServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="04a96-101">New-AzCloudServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="04a96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04a96-102">SYNOPSIS</span></span>
<span data-ttu-id="04a96-103">Memória-objektum létrehozása diagnosztikai bővítményhez</span><span class="sxs-lookup"><span data-stu-id="04a96-103">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="04a96-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="04a96-104">SYNTAX</span></span>

```
New-AzCloudServiceDiagnosticsExtension [-Name] <String> [-ResourceGroupName] <String>
 [-CloudServiceName] <String> [-DiagnosticsConfigurationPath] <String> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [[-Subscription] <String>] [[-TypeHandlerVersion] <String>]
 [[-RolesAppliedTo] <String[]>] [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="04a96-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="04a96-105">DESCRIPTION</span></span>
<span data-ttu-id="04a96-106">Memória-objektum létrehozása diagnosztikai bővítményhez</span><span class="sxs-lookup"><span data-stu-id="04a96-106">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="04a96-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="04a96-107">EXAMPLES</span></span>

### <span data-ttu-id="04a96-108">1. példa: Diagnosztikai bővítményobjektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="04a96-108">Example 1: Create diagnostics extension object</span></span>
```powershell
PS C:\> $storageAccountKey = Get-AzStorageAccountKey -ResourceGroupName "ContosOrg" -Name "ContosSA"
PS C:\> $configFile = "<WAD configuration file path>"
PS C:\> $extension = New-AzCloudServiceDiagnosticsExtension -Name "WADExtension" -ResourceGroupName "ContosOrg" -CloudServiceName "ContosCS" -StorageAccountName "ContosSA" -StorageAccountKey $storageAccountKey[0].Value -DiagnosticsConfigurationPath $configFile -TypeHandlerVersion "1.5" -AutoUpgradeMinorVersion $true
```

<span data-ttu-id="04a96-109">Ez a parancs diagnosztikai bővítményobjektumot hoz létre, amely egy felhőszolgáltatás létrehozására vagy frissítésére használható.</span><span class="sxs-lookup"><span data-stu-id="04a96-109">This command creates diagnostics extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="04a96-110">További részletekért lásd: New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="04a96-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="04a96-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04a96-111">PARAMETERS</span></span>

### <span data-ttu-id="04a96-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="04a96-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="04a96-113">Alverzió automatikus frissítése.</span><span class="sxs-lookup"><span data-stu-id="04a96-113">Auto upgrade minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a96-114">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="04a96-114">-CloudServiceName</span></span>
<span data-ttu-id="04a96-115">A felhőszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="04a96-115">Name of Cloud Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a96-116">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="04a96-116">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="04a96-117">Az Azure Diagnostics konfigurációját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="04a96-117">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="04a96-118">A sémát a következő paranccsal töltheti le: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics'). PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'</span><span class="sxs-lookup"><span data-stu-id="04a96-118">You can download the schema by using the following command: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a96-119">-Name</span><span class="sxs-lookup"><span data-stu-id="04a96-119">-Name</span></span>
<span data-ttu-id="04a96-120">A diagnosztikai bővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="04a96-120">Name of Diagnostics Extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a96-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04a96-121">-ResourceGroupName</span></span>
<span data-ttu-id="04a96-122">A felhőszolgáltatás erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="04a96-122">Resource Group name of Cloud Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a96-123">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="04a96-123">-RolesAppliedTo</span></span>
<span data-ttu-id="04a96-124">Az alkalmazott szerepkörök.</span><span class="sxs-lookup"><span data-stu-id="04a96-124">Roles applied to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a96-125">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="04a96-125">-StorageAccountKey</span></span>
<span data-ttu-id="04a96-126">Tárfiók kulcsa.</span><span class="sxs-lookup"><span data-stu-id="04a96-126">Storage Account Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a96-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="04a96-127">-StorageAccountName</span></span>
<span data-ttu-id="04a96-128">A tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="04a96-128">Name of the Storage Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a96-129">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="04a96-129">-Subscription</span></span>
<span data-ttu-id="04a96-130">Előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04a96-130">Subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a96-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="04a96-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="04a96-132">A bővítmény verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="04a96-132">Specifies the version of the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a96-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04a96-133">CommonParameters</span></span>
<span data-ttu-id="04a96-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04a96-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04a96-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04a96-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04a96-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04a96-136">INPUTS</span></span>

## <span data-ttu-id="04a96-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04a96-137">OUTPUTS</span></span>

### <span data-ttu-id="04a96-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="04a96-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="04a96-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="04a96-139">NOTES</span></span>

<span data-ttu-id="04a96-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="04a96-140">ALIASES</span></span>

## <span data-ttu-id="04a96-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04a96-141">RELATED LINKS</span></span>

