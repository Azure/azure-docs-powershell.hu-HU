---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 04454028957dfee3c7d50c47341be7e979ed3a9f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017821"
---
# <span data-ttu-id="1d0d8-101">Remove-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="1d0d8-101">Remove-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="1d0d8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d0d8-102">SYNOPSIS</span></span>
<span data-ttu-id="1d0d8-103">szinkronizálási beállítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1d0d8-103">removes a synchronization setting</span></span>

## <span data-ttu-id="1d0d8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d0d8-104">SYNTAX</span></span>

### <span data-ttu-id="1d0d8-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1d0d8-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1d0d8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d0d8-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d0d8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d0d8-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -InputObject <PSDataShareSynchronizationSetting> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d0d8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d0d8-108">DESCRIPTION</span></span>
<span data-ttu-id="1d0d8-109">A **Remove-AzDataShareSynchronizationSetting** parancsmag eltávolítja a DataShare szinkronizálási beállítását</span><span class="sxs-lookup"><span data-stu-id="1d0d8-109">The **Remove-AzDataShareSynchronizationSetting** cmdlet removes a datashare synchronization setting</span></span>

## <span data-ttu-id="1d0d8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1d0d8-110">EXAMPLES</span></span>

### <span data-ttu-id="1d0d8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1d0d8-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsShareSynchronizationSetting"

Are you sure you want to remove synchronization-setting "AdsShareSynchronizationSetting"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="1d0d8-112">Ez a parancs eltávolítja a AdsShareSynchronizationSetting nevű szinkronizálási beállítást a megosztási AdsShare.</span><span class="sxs-lookup"><span data-stu-id="1d0d8-112">This commands removes a synchronization setting named AdsShareSynchronizationSetting from share AdsShare.</span></span> 

## <span data-ttu-id="1d0d8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d0d8-113">PARAMETERS</span></span>

### <span data-ttu-id="1d0d8-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1d0d8-114">-AccountName</span></span>
<span data-ttu-id="1d0d8-115">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="1d0d8-115">Azure Data Share Account name</span></span>

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

### <span data-ttu-id="1d0d8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d0d8-116">-AsJob</span></span>
<span data-ttu-id="1d0d8-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="1d0d8-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="1d0d8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d0d8-118">-DefaultProfile</span></span>
<span data-ttu-id="1d0d8-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d0d8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d0d8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d0d8-120">-InputObject</span></span>
<span data-ttu-id="1d0d8-121">Az Azure Data Share szinkronizálási beállítása.</span><span class="sxs-lookup"><span data-stu-id="1d0d8-121">The Azure Data Share Synchronization setting.</span></span>


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

### <span data-ttu-id="1d0d8-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1d0d8-122">-Name</span></span>
<span data-ttu-id="1d0d8-123">Szinkronizálási beállítás neve</span><span class="sxs-lookup"><span data-stu-id="1d0d8-123">Synchronization setting name</span></span>

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

### <span data-ttu-id="1d0d8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d0d8-124">-PassThru</span></span>
<span data-ttu-id="1d0d8-125">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="1d0d8-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="1d0d8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d0d8-126">-ResourceGroupName</span></span>
<span data-ttu-id="1d0d8-127">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="1d0d8-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="1d0d8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d0d8-128">-ResourceId</span></span>
<span data-ttu-id="1d0d8-129">A szinkronizálási beállítás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="1d0d8-129">The resource id of the synchronization setting</span></span>

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

### <span data-ttu-id="1d0d8-130">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="1d0d8-130">-ShareName</span></span>
<span data-ttu-id="1d0d8-131">Azure-adatmegosztás neve</span><span class="sxs-lookup"><span data-stu-id="1d0d8-131">Azure data share name</span></span>

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

### <span data-ttu-id="1d0d8-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1d0d8-132">-Confirm</span></span>
<span data-ttu-id="1d0d8-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1d0d8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d0d8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d0d8-134">-WhatIf</span></span>
<span data-ttu-id="1d0d8-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1d0d8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d0d8-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1d0d8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d0d8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d0d8-137">CommonParameters</span></span>
<span data-ttu-id="1d0d8-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d0d8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d0d8-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1d0d8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d0d8-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d0d8-140">INPUTS</span></span>

### <span data-ttu-id="1d0d8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1d0d8-141">System.String</span></span>

### <span data-ttu-id="1d0d8-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="1d0d8-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="1d0d8-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d0d8-143">OUTPUTS</span></span>

### <span data-ttu-id="1d0d8-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1d0d8-144">System.Boolean</span></span>

## <span data-ttu-id="1d0d8-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d0d8-145">NOTES</span></span>

## <span data-ttu-id="1d0d8-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d0d8-146">RELATED LINKS</span></span>
