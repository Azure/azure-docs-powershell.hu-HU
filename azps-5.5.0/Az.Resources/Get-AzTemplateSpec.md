---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160010"
---
# <span data-ttu-id="f49ba-101">Get-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="f49ba-101">Get-AzTemplateSpec</span></span>

## <span data-ttu-id="f49ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f49ba-102">SYNOPSIS</span></span>
<span data-ttu-id="f49ba-103">Sablon specifikációi</span><span class="sxs-lookup"><span data-stu-id="f49ba-103">Gets or lists Template Specs</span></span>

## <span data-ttu-id="f49ba-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f49ba-104">SYNTAX</span></span>

### <span data-ttu-id="f49ba-105">ListTemplateSpecsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f49ba-105">ListTemplateSpecsParameterSet (Default)</span></span>
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f49ba-106">GetTemplateSpecByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f49ba-106">GetTemplateSpecByNameParameterSet</span></span>
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f49ba-107">GetTemplateSpecByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f49ba-107">GetTemplateSpecByIdParameterSet</span></span>
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f49ba-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f49ba-108">DESCRIPTION</span></span>
<span data-ttu-id="f49ba-109">Ez a parancsmag használható sablon specifikációk listához egy előfizetés/erőforráscsoportban, vagy egy adott sablon specifikációjának lekérthez név vagy azonosító alapján. Ha egy adott sablont név/azonosító alapján kap meg, a **-Version** paraméterben megadott verziónév megadásával szükség esetén lekérhet egy adott verziót.</span><span class="sxs-lookup"><span data-stu-id="f49ba-109">This cmdlet can be used to list Template Specs in a subscription/resource group or get a specific Template Spec by name or id. When getting a specific Template Spec by name/id a specific version can optionally be retrieved by specifying a version name through the **-Version** parameter.</span></span> <span data-ttu-id="f49ba-110">A **-Version** (Verzió) használata esetén csak az adott verzió részletei lesznek jelen a \**verzióban. A visszaadott* Template Spec objektum verziószámai.</span><span class="sxs-lookup"><span data-stu-id="f49ba-110">When **-Version** is used, only the specific version details will be present within \**.Versions* on the returned Template Spec object.</span></span> <span data-ttu-id="f49ba-111">Ha a Sablon specifikációjának név/azonosító alapján való beolvasásakor nincs megadva adott verzió, az összes verzió a \* értéken belül fog *jelenni. A visszaadott* objektum Verziótulajdonság.</span><span class="sxs-lookup"><span data-stu-id="f49ba-111">If no specific version is specified when retrieving a Template Spec by name/id, all versions will be present within the  \**.Versions* property of the returned object.</span></span>

<span data-ttu-id="f49ba-112">**Megjegyzés:** Amikor egy előfizetés vagy erőforráscsoport összes sablon specifikációját felsorolja, minden egyes visszaadott sablon specifikációja *". A Versions"* tulajdonság *null értékű* lesz.</span><span class="sxs-lookup"><span data-stu-id="f49ba-112">**Note**: When listing all Template Specs within a subscription or resource group, each returned Template Spec's *".Versions"* property will be *null*.</span></span> <span data-ttu-id="f49ba-113">A verzióinformációk csak akkor szerepelnek itt, ha -Name vagy -ResourceId paramétert ad meg (például: egy adott sablon specifikációját/verzióját kéri).</span><span class="sxs-lookup"><span data-stu-id="f49ba-113">Version information is only included when -Name or -ResourceId parameters are provided (eg: you are requesting a specific template spec/version).</span></span>

## <span data-ttu-id="f49ba-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f49ba-114">EXAMPLES</span></span>

### <span data-ttu-id="f49ba-115">1. példa: Listasablon specifikációi az aktuális előfizetésben</span><span class="sxs-lookup"><span data-stu-id="f49ba-115">Example 1: List Template Specs in current subscription</span></span>
```powershell
PS C:\> Get-AzTemplateSpec
```

<span data-ttu-id="f49ba-116">Az aktuális előfizetés összes sablon specifikációját felsorolja.</span><span class="sxs-lookup"><span data-stu-id="f49ba-116">Lists all Template Specs in the current subscription.</span></span>

### <span data-ttu-id="f49ba-117">2. példa: List Template Specs in a resource group</span><span class="sxs-lookup"><span data-stu-id="f49ba-117">Example 2: List Template Specs in a resource group</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

<span data-ttu-id="f49ba-118">Az aktuális előfizetés "myRG" erőforráscsoportjának sablon specifikációit sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="f49ba-118">Lists all Template Specs in the resource group 'myRG' of the current subscription.</span></span>

### <span data-ttu-id="f49ba-119">3. példa: Sablon specifikációjának lekérte (az összes verzióval) név szerint</span><span class="sxs-lookup"><span data-stu-id="f49ba-119">Example 3: Get Template Spec (with all versions) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="f49ba-120">Információkat kap a "MyTemplateSpec" nevű sablon specifikációról a "myRG" erőforráscsoporton belül.</span><span class="sxs-lookup"><span data-stu-id="f49ba-120">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="f49ba-121">**Megjegyzés:** A Sablon specifikációjának összes verziója a *". A visszatérési* objektum Versions " tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="f49ba-121">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="f49ba-122">4. példa: Sablon specifikációjának (adott verzió) lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="f49ba-122">Example 4: Get Template Spec (specific version) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="f49ba-123">Információkat kap a "MyTemplateSpec" nevű sablon specifikációjának "v1.0" verziójáról a "myRG" erőforráscsoporton belül.</span><span class="sxs-lookup"><span data-stu-id="f49ba-123">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="f49ba-124">**Megjegyzés:** A *". A visszaadott objektum Versions"* tulajdonsága csak a kért verziót fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="f49ba-124">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

### <span data-ttu-id="f49ba-125">5. példa: Sablon specifikációjának lekérte (az összes verzióval) erőforrás-azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="f49ba-125">Example 5: Get Template Spec (with all versions) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

<span data-ttu-id="f49ba-126">Információkat kap a "MyTemplateSpec" nevű sablon specifikációról az előfizetési alazonosító "myRG" \{ erőforráscsoportján \} belül.</span><span class="sxs-lookup"><span data-stu-id="f49ba-126">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="f49ba-127">**Megjegyzés:** A Sablon specifikációjának összes verziója a *". A visszatérési* objektum Versions " tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="f49ba-127">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="f49ba-128">6. példa: Sablon specifikációjának (adott verzió) lekérte erőforrás-azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="f49ba-128">Example 6: Get Template Spec (specific version) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="f49ba-129">Információkat kap a "MyTemplateSpec" nevű sablon specifikációjának "v1.0" verziójáról az előfizetési alazonosító "myRG" \{ erőforráscsoportján \} belül.</span><span class="sxs-lookup"><span data-stu-id="f49ba-129">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="f49ba-130">**Megjegyzés:** A *". A visszaadott objektum Versions"* tulajdonsága csak a kért verziót fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="f49ba-130">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

## <span data-ttu-id="f49ba-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f49ba-131">PARAMETERS</span></span>

### <span data-ttu-id="f49ba-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f49ba-132">-DefaultProfile</span></span>
<span data-ttu-id="f49ba-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f49ba-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f49ba-134">-Name</span><span class="sxs-lookup"><span data-stu-id="f49ba-134">-Name</span></span>
<span data-ttu-id="f49ba-135">A sablon specifikációjának neve.</span><span class="sxs-lookup"><span data-stu-id="f49ba-135">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f49ba-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f49ba-136">-ResourceGroupName</span></span>
<span data-ttu-id="f49ba-137">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f49ba-137">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListTemplateSpecsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f49ba-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f49ba-138">-ResourceId</span></span>
<span data-ttu-id="f49ba-139">A sablon specifikációjának teljesen minősített erőforrás-azonosítója. Példa: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="f49ba-139">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f49ba-140">-Verzió</span><span class="sxs-lookup"><span data-stu-id="f49ba-140">-Version</span></span>
<span data-ttu-id="f49ba-141">A sablon specifikációjának verziója.</span><span class="sxs-lookup"><span data-stu-id="f49ba-141">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet, GetTemplateSpecByIdParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f49ba-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f49ba-142">CommonParameters</span></span>
<span data-ttu-id="f49ba-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f49ba-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f49ba-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f49ba-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f49ba-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f49ba-145">INPUTS</span></span>

### <span data-ttu-id="f49ba-146">System.String</span><span class="sxs-lookup"><span data-stu-id="f49ba-146">System.String</span></span>

## <span data-ttu-id="f49ba-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f49ba-147">OUTPUTS</span></span>

### <span data-ttu-id="f49ba-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="f49ba-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="f49ba-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f49ba-149">NOTES</span></span>

## <span data-ttu-id="f49ba-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f49ba-150">RELATED LINKS</span></span>
