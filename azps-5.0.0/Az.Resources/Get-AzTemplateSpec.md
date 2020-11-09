---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301073"
---
# <span data-ttu-id="71e9a-101">Get-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="71e9a-101">Get-AzTemplateSpec</span></span>

## <span data-ttu-id="71e9a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="71e9a-103">Sablonok specifikációjának beolvasása vagy listázása</span><span class="sxs-lookup"><span data-stu-id="71e9a-103">Gets or lists Template Specs</span></span>

## <span data-ttu-id="71e9a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71e9a-104">SYNTAX</span></span>

### <span data-ttu-id="71e9a-105">ListTemplateSpecsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="71e9a-105">ListTemplateSpecsParameterSet (Default)</span></span>
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71e9a-106">GetTemplateSpecByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="71e9a-106">GetTemplateSpecByNameParameterSet</span></span>
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71e9a-107">GetTemplateSpecByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71e9a-107">GetTemplateSpecByIdParameterSet</span></span>
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="71e9a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="71e9a-108">DESCRIPTION</span></span>
<span data-ttu-id="71e9a-109">Ez a parancsmag használható az előfizetésben/erőforrás csoportban lévő sablon specifikációjának listázására, illetve egy adott sablon specifikációjának vagy azonosítójának beszerzésére. Ha egy adott verziót egy adott verzióval egy adott verzióval egy adott verzióra, akkor a verziószámot a **verziószám paraméterrel** kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="71e9a-109">This cmdlet can be used to list Template Specs in a subscription/resource group or get a specific Template Spec by name or id. When getting a specific Template Spec by name/id a specific version can optionally be retrieved by specifying a version name through the **-Version** parameter.</span></span> <span data-ttu-id="71e9a-110">A **verzió** használatakor a program csak az adott verzió részleteit fogja tartalmazni a \*-ban *.* A visszaadott sablon spec objektumának verziószáma.</span><span class="sxs-lookup"><span data-stu-id="71e9a-110">When **-Version** is used, only the specific version details will be present within \* *.Versions* on the returned Template Spec object.</span></span> <span data-ttu-id="71e9a-111">Ha nem ad meg konkrét verziót, ha a sablont egy név vagy azonosító szerint adja meg, akkor minden verzió megtalálható lesz a \* címen *.* A visszaadott objektum verziói tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="71e9a-111">If no specific version is specified when retrieving a Template Spec by name/id, all versions will be present within the  \* *.Versions* property of the returned object.</span></span>

<span data-ttu-id="71e9a-112">**Megjegyzés** : Ha az előfizetésben vagy az erőforrás csoportban található minden sablonra vonatkozó specifikációt ad meg, a program minden olyan sablont ad vissza *. A Versions* tulajdonság *értéke null* lesz.</span><span class="sxs-lookup"><span data-stu-id="71e9a-112">**Note** : When listing all Template Specs within a subscription or resource group, each returned Template Spec's *".Versions"* property will be *null*.</span></span> <span data-ttu-id="71e9a-113">A verziós adatok csak akkor jelennek meg, ha-Name vagy-ResourceId paramétereket tartalmaz (például: egy adott sablont kér a spec/Version).</span><span class="sxs-lookup"><span data-stu-id="71e9a-113">Version information is only included when -Name or -ResourceId parameters are provided (eg: you are requesting a specific template spec/version).</span></span>

## <span data-ttu-id="71e9a-114">Példák</span><span class="sxs-lookup"><span data-stu-id="71e9a-114">EXAMPLES</span></span>

### <span data-ttu-id="71e9a-115">1. példa: a lista sablon specifikációi a jelenlegi előfizetésben</span><span class="sxs-lookup"><span data-stu-id="71e9a-115">Example 1: List Template Specs in current subscription</span></span>
```powershell
PS C:\> Get-AzTemplateSpec
```

<span data-ttu-id="71e9a-116">Felsorolja az összes sablon specifikációját a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="71e9a-116">Lists all Template Specs in the current subscription.</span></span>

### <span data-ttu-id="71e9a-117">2. példa: egy erőforráscsoport lista sablon specifikációja</span><span class="sxs-lookup"><span data-stu-id="71e9a-117">Example 2: List Template Specs in a resource group</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

<span data-ttu-id="71e9a-118">Felsorolja az összes sablon specifikációját az aktuális előfizetés erőforráscsoport "myRG" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="71e9a-118">Lists all Template Specs in the resource group 'myRG' of the current subscription.</span></span>

### <span data-ttu-id="71e9a-119">3. példa: a sablon specifikációjának beszerzése (minden verzióval) név szerint</span><span class="sxs-lookup"><span data-stu-id="71e9a-119">Example 3: Get Template Spec (with all versions) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="71e9a-120">Információt kap a "MyTemplateSpec" nevű "myRG" erőforráscsoporthoz tartozó "" nevű sablonról.</span><span class="sxs-lookup"><span data-stu-id="71e9a-120">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="71e9a-121">**Megjegyzés** : az összes sablon specifikációjának verziószáma a következő lesz: " *.* A feladó objektum verzió tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="71e9a-121">**Note** : All of the Template Spec's versions will be present within the " *.Versions* " property of the return object.</span></span>

### <span data-ttu-id="71e9a-122">Példa 4: a sablon specifikációjának beszerzése (adott verzió) név szerint</span><span class="sxs-lookup"><span data-stu-id="71e9a-122">Example 4: Get Template Spec (specific version) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="71e9a-123">Információt kap a ' MyTemplateSpec ' nevű "myRG" erőforráscsoporthoz tartozó "" nevű sablon "v 1.0" verziójáról.</span><span class="sxs-lookup"><span data-stu-id="71e9a-123">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="71e9a-124">**Megjegyzés** : a *".* A visszaadott objektum (verziók) tulajdonsága csak a kért verziót fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="71e9a-124">**Note** : The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

### <span data-ttu-id="71e9a-125">Példa 5: erőforrás-azonosító lekérése a sablonhoz (minden verzióval)</span><span class="sxs-lookup"><span data-stu-id="71e9a-125">Example 5: Get Template Spec (with all versions) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

<span data-ttu-id="71e9a-126">Információt kap az "MyTemplateSpec" nevű "" nevű sablonról az előfizetés subId erőforráscsoport "myRG" csoportjában \{ \} .</span><span class="sxs-lookup"><span data-stu-id="71e9a-126">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="71e9a-127">**Megjegyzés** : az összes sablon specifikációjának verziószáma a következő lesz: " *.* A feladó objektum verzió tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="71e9a-127">**Note** : All of the Template Spec's versions will be present within the " *.Versions* " property of the return object.</span></span>

### <span data-ttu-id="71e9a-128">Példa 6: erőforrás-azonosító (adott verzió) beolvasása erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="71e9a-128">Example 6: Get Template Spec (specific version) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="71e9a-129">Információt kap az "MyTemplateSpec" nevű "myRG" nevű erőforráscsoport "v 1.0" verziójáról az előfizetés \{ subId \} .</span><span class="sxs-lookup"><span data-stu-id="71e9a-129">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="71e9a-130">**Megjegyzés** : a *".* A visszaadott objektum (verziók) tulajdonsága csak a kért verziót fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="71e9a-130">**Note** : The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

## <span data-ttu-id="71e9a-131">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71e9a-131">PARAMETERS</span></span>

### <span data-ttu-id="71e9a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e9a-132">-DefaultProfile</span></span>
<span data-ttu-id="71e9a-133">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71e9a-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71e9a-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="71e9a-134">-Name</span></span>
<span data-ttu-id="71e9a-135">Annak a sablonnak a neve, amely a spec nevet adja.</span><span class="sxs-lookup"><span data-stu-id="71e9a-135">The name of the template spec.</span></span>

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

### <span data-ttu-id="71e9a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71e9a-136">-ResourceGroupName</span></span>
<span data-ttu-id="71e9a-137">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="71e9a-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="71e9a-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71e9a-138">-ResourceId</span></span>
<span data-ttu-id="71e9a-139">A sablon teljes értékű erőforrás-azonosítója (példa:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName})</span><span class="sxs-lookup"><span data-stu-id="71e9a-139">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="71e9a-140">-Verzió</span><span class="sxs-lookup"><span data-stu-id="71e9a-140">-Version</span></span>
<span data-ttu-id="71e9a-141">A sablon specifikációjának verziója.</span><span class="sxs-lookup"><span data-stu-id="71e9a-141">The version of the template spec.</span></span>

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

### <span data-ttu-id="71e9a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e9a-142">CommonParameters</span></span>
<span data-ttu-id="71e9a-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71e9a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e9a-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="71e9a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e9a-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71e9a-145">INPUTS</span></span>

### <span data-ttu-id="71e9a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="71e9a-146">System.String</span></span>

## <span data-ttu-id="71e9a-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71e9a-147">OUTPUTS</span></span>

### <span data-ttu-id="71e9a-148">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="71e9a-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="71e9a-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71e9a-149">NOTES</span></span>

## <span data-ttu-id="71e9a-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71e9a-150">RELATED LINKS</span></span>
