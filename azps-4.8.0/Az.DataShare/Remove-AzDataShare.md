---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 2679a3f63be3b7332020354e325e33573911334b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024050"
---
# <span data-ttu-id="1c3b4-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="1c3b4-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="1c3b4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1c3b4-102">SYNOPSIS</span></span>
<span data-ttu-id="1c3b4-103">Eltávolítja az adatmegosztást.</span><span class="sxs-lookup"><span data-stu-id="1c3b4-103">Removes a data share.</span></span>

## <span data-ttu-id="1c3b4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1c3b4-104">SYNTAX</span></span>

### <span data-ttu-id="1c3b4-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1c3b4-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c3b4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c3b4-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c3b4-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c3b4-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c3b4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1c3b4-108">DESCRIPTION</span></span>
<span data-ttu-id="1c3b4-109">A **Remove-AzDataShare** parancsmag eltávolítja az adatmegosztást.</span><span class="sxs-lookup"><span data-stu-id="1c3b4-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="1c3b4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1c3b4-110">EXAMPLES</span></span>

### <span data-ttu-id="1c3b4-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1c3b4-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="1c3b4-112">Ez a parancs eltávolítja a AdsShare nevű adatmegosztást az Azure Data Share-fiók WikiAds.</span><span class="sxs-lookup"><span data-stu-id="1c3b4-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="1c3b4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1c3b4-113">PARAMETERS</span></span>

### <span data-ttu-id="1c3b4-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1c3b4-114">-AccountName</span></span>
<span data-ttu-id="1c3b4-115">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="1c3b4-115">Azure data share account name</span></span>

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

### <span data-ttu-id="1c3b4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c3b4-116">-AsJob</span></span>
<span data-ttu-id="1c3b4-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="1c3b4-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="1c3b4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c3b4-118">-DefaultProfile</span></span>
<span data-ttu-id="1c3b4-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1c3b4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c3b4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c3b4-120">-InputObject</span></span>
<span data-ttu-id="1c3b4-121">Azure Data Share Object ' ' ' YAML típusa: PSDataShare paraméter-készletek: ByObjectParameterSet aliasok:</span><span class="sxs-lookup"><span data-stu-id="1c3b4-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="1c3b4-122">Kötelező: igaz pozíció: névvel ellátott alapértelmezett érték: nincs elfogadás csővezeték-bevitel: igaz (ByValue) elfogadja a helyettesítő karaktereket: false</span><span class="sxs-lookup"><span data-stu-id="1c3b4-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c3b4-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1c3b4-123">-Name</span></span>
<span data-ttu-id="1c3b4-124">Azure-adatmegosztás neve</span><span class="sxs-lookup"><span data-stu-id="1c3b4-124">Azure data share name</span></span>

<span data-ttu-id="1c3b4-125">YAML típusa: karakterlánc-paraméterek halmaza: ByFieldsParameterSet aliasok:</span><span class="sxs-lookup"><span data-stu-id="1c3b4-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="1c3b4-126">Kötelező: igaz pozíció: elnevezett alapértelmezett érték: nincs elfogadás csővezeték-bevitel: false Accept helyettesítő karakterek: false</span><span class="sxs-lookup"><span data-stu-id="1c3b4-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="1c3b4-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c3b4-127">-PassThru</span></span>
<span data-ttu-id="1c3b4-128">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="1c3b4-128">Return object (if specified).</span></span>

<span data-ttu-id="1c3b4-129">YAML típus: SwitchParameter paraméterek: (all) aliasok:</span><span class="sxs-lookup"><span data-stu-id="1c3b4-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="1c3b4-130">Kötelező: hamis pozíció: elnevezett alapértelmezett érték: nincs elfogadás csővezeték-bevitel: false Accept helyettesítő karakterek: false</span><span class="sxs-lookup"><span data-stu-id="1c3b4-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="1c3b4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c3b4-131">-ResourceGroupName</span></span>
<span data-ttu-id="1c3b4-132">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="1c3b4-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="1c3b4-133">YAML típusa: karakterlánc-paraméterek halmaza: ByFieldsParameterSet aliasok:</span><span class="sxs-lookup"><span data-stu-id="1c3b4-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="1c3b4-134">Kötelező: igaz pozíció: elnevezett alapértelmezett érték: nincs elfogadás csővezeték-bevitel: false Accept helyettesítő karakterek: false</span><span class="sxs-lookup"><span data-stu-id="1c3b4-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="1c3b4-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c3b4-135">-ResourceId</span></span>
<span data-ttu-id="1c3b4-136">Az Azure-adatmegosztás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="1c3b4-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="1c3b4-137">YAML típusa: karakterlánc-paraméterek halmaza: ByResourceIdParameterSet aliasok:</span><span class="sxs-lookup"><span data-stu-id="1c3b4-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="1c3b4-138">Kötelező: igaz pozíció: névvel ellátott alapértelmezett érték: nincs elfogadás csővezeték-bevitel: igaz (ByPropertyName) elfogadja a helyettesítő karaktereket: false</span><span class="sxs-lookup"><span data-stu-id="1c3b4-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="1c3b4-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1c3b4-139">-Confirm</span></span>
<span data-ttu-id="1c3b4-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1c3b4-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="1c3b4-141">YAML típus: SwitchParameter paraméterek: (all) aliasok: CF</span><span class="sxs-lookup"><span data-stu-id="1c3b4-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="1c3b4-142">Kötelező: hamis pozíció: elnevezett alapértelmezett érték: nincs elfogadás csővezeték-bevitel: false Accept helyettesítő karakterek: false</span><span class="sxs-lookup"><span data-stu-id="1c3b4-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="1c3b4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c3b4-143">-WhatIf</span></span>
<span data-ttu-id="1c3b4-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1c3b4-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c3b4-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1c3b4-145">The cmdlet is not run.</span></span>

<span data-ttu-id="1c3b4-146">YAML típus: SwitchParameter paraméterek: (all) aliasok: Wi</span><span class="sxs-lookup"><span data-stu-id="1c3b4-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="1c3b4-147">Kötelező: hamis pozíció: elnevezett alapértelmezett érték: nincs elfogadás csővezeték-bevitel: false Accept helyettesítő karakterek: false</span><span class="sxs-lookup"><span data-stu-id="1c3b4-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>




<span data-ttu-id="1c3b4-148">YAML típusa: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare paraméter: ByObjectParameterSet aliasok:</span><span class="sxs-lookup"><span data-stu-id="1c3b4-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span>

<span data-ttu-id="1c3b4-149">Kötelező: igaz pozíció: névvel ellátott alapértelmezett érték: nincs elfogadás csővezeték-bevitel: igaz (ByValue) elfogadja a helyettesítő karaktereket: false</span><span class="sxs-lookup"><span data-stu-id="1c3b4-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="1c3b4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c3b4-150">CommonParameters</span></span>
<span data-ttu-id="1c3b4-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1c3b4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c3b4-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1c3b4-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c3b4-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c3b4-153">INPUTS</span></span>

### <span data-ttu-id="1c3b4-154">System. String</span><span class="sxs-lookup"><span data-stu-id="1c3b4-154">System.String</span></span>

### <span data-ttu-id="1c3b4-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="1c3b4-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="1c3b4-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c3b4-156">OUTPUTS</span></span>

### <span data-ttu-id="1c3b4-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1c3b4-157">System.Boolean</span></span>

## <span data-ttu-id="1c3b4-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1c3b4-158">NOTES</span></span>

## <span data-ttu-id="1c3b4-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c3b4-159">RELATED LINKS</span></span>
