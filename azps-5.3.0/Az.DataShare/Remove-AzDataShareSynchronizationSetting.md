---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 04454028957dfee3c7d50c47341be7e979ed3a9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377101"
---
# <span data-ttu-id="15099-101">Remove-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="15099-101">Remove-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="15099-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15099-102">SYNOPSIS</span></span>
<span data-ttu-id="15099-103">szinkronizálási beállítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="15099-103">removes a synchronization setting</span></span>

## <span data-ttu-id="15099-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="15099-104">SYNTAX</span></span>

### <span data-ttu-id="15099-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="15099-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15099-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15099-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15099-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15099-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -InputObject <PSDataShareSynchronizationSetting> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15099-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="15099-108">DESCRIPTION</span></span>
<span data-ttu-id="15099-109">A **Remove-AzDataShareSynchronizationSetting** parancsmag eltávolítja az adatmegosztás szinkronizálási beállítását</span><span class="sxs-lookup"><span data-stu-id="15099-109">The **Remove-AzDataShareSynchronizationSetting** cmdlet removes a datashare synchronization setting</span></span>

## <span data-ttu-id="15099-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="15099-110">EXAMPLES</span></span>

### <span data-ttu-id="15099-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="15099-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsShareSynchronizationSetting"

Are you sure you want to remove synchronization-setting "AdsShareSynchronizationSetting"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="15099-112">Ez a parancs eltávolítja az AdsShareSynchronizationSetting nevű szinkronizálási beállítást a Share AdsShare szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="15099-112">This commands removes a synchronization setting named AdsShareSynchronizationSetting from share AdsShare.</span></span> 

## <span data-ttu-id="15099-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15099-113">PARAMETERS</span></span>

### <span data-ttu-id="15099-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="15099-114">-AccountName</span></span>
<span data-ttu-id="15099-115">Azure Data Share Account name</span><span class="sxs-lookup"><span data-stu-id="15099-115">Azure Data Share Account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15099-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15099-116">-AsJob</span></span>
<span data-ttu-id="15099-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="15099-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="15099-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15099-118">-DefaultProfile</span></span>
<span data-ttu-id="15099-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15099-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15099-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15099-120">-InputObject</span></span>
<span data-ttu-id="15099-121">Az Azure Data Share Synchronization beállítás.</span><span class="sxs-lookup"><span data-stu-id="15099-121">The Azure Data Share Synchronization setting.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15099-122">-Name</span><span class="sxs-lookup"><span data-stu-id="15099-122">-Name</span></span>
<span data-ttu-id="15099-123">Szinkronizálási beállítás neve</span><span class="sxs-lookup"><span data-stu-id="15099-123">Synchronization setting name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15099-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15099-124">-PassThru</span></span>
<span data-ttu-id="15099-125">Visszatérési objektum (ha meg van adva).</span><span class="sxs-lookup"><span data-stu-id="15099-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="15099-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15099-126">-ResourceGroupName</span></span>
<span data-ttu-id="15099-127">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="15099-127">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15099-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15099-128">-ResourceId</span></span>
<span data-ttu-id="15099-129">A szinkronizálási beállítás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="15099-129">The resource id of the synchronization setting</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15099-130">-ShareName</span><span class="sxs-lookup"><span data-stu-id="15099-130">-ShareName</span></span>
<span data-ttu-id="15099-131">Azure-adatok megosztásának neve</span><span class="sxs-lookup"><span data-stu-id="15099-131">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15099-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15099-132">-Confirm</span></span>
<span data-ttu-id="15099-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="15099-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15099-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15099-134">-WhatIf</span></span>
<span data-ttu-id="15099-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="15099-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15099-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="15099-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15099-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15099-137">CommonParameters</span></span>
<span data-ttu-id="15099-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15099-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15099-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15099-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15099-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="15099-140">INPUTS</span></span>

### <span data-ttu-id="15099-141">System.String</span><span class="sxs-lookup"><span data-stu-id="15099-141">System.String</span></span>

### <span data-ttu-id="15099-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="15099-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="15099-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15099-143">OUTPUTS</span></span>

### <span data-ttu-id="15099-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="15099-144">System.Boolean</span></span>

## <span data-ttu-id="15099-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="15099-145">NOTES</span></span>

## <span data-ttu-id="15099-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15099-146">RELATED LINKS</span></span>
