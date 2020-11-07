---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
ms.openlocfilehash: a6fa8a27bacf5504564703d8669616f748aa95d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679943"
---
# <span data-ttu-id="c259f-101">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c259f-101">Set-AzureRmResourceGroup</span></span>

## <span data-ttu-id="c259f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c259f-102">SYNOPSIS</span></span>
<span data-ttu-id="c259f-103">Egy erőforráscsoport módosítása</span><span class="sxs-lookup"><span data-stu-id="c259f-103">Modifies a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c259f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c259f-104">SYNTAX</span></span>

### <span data-ttu-id="c259f-105">A név alapján jeleníti meg az erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="c259f-105">Lists the resource group based in the name.</span></span> <span data-ttu-id="c259f-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="c259f-106">(Default)</span></span>
```
Set-AzureRmResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c259f-107">Felsorolja az azonosító alapján az erőforráscsoport listáját.</span><span class="sxs-lookup"><span data-stu-id="c259f-107">Lists the resource group based in the Id.</span></span>
```
Set-AzureRmResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c259f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c259f-108">DESCRIPTION</span></span>
<span data-ttu-id="c259f-109">A **set-AzureRmResourceGroup** parancsmag egy erőforráscsoport tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="c259f-109">The **Set-AzureRmResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="c259f-110">Ezzel a parancsmaggal megadhatja, módosíthatja vagy törölheti az erőforrás-csoportokra alkalmazott Azure-címkéket.</span><span class="sxs-lookup"><span data-stu-id="c259f-110">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="c259f-111">Adja meg a *Name (név* ) paramétert az erőforráscsoport meghatározásához, illetve a *címke* paramétert a címkék módosításához.</span><span class="sxs-lookup"><span data-stu-id="c259f-111">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>

<span data-ttu-id="c259f-112">Ez a parancsmag nem használható az erőforráscsoport nevének módosítására.</span><span class="sxs-lookup"><span data-stu-id="c259f-112">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="c259f-113">Példák</span><span class="sxs-lookup"><span data-stu-id="c259f-113">EXAMPLES</span></span>

### <span data-ttu-id="c259f-114">1. példa: címke alkalmazása erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="c259f-114">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="c259f-115">Ez a parancs egy olyan részleg címkét alkalmaz, amelynek az értéke egy olyan erőforráscsoport, amely nem tartalmaz meglévő címkéket.</span><span class="sxs-lookup"><span data-stu-id="c259f-115">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="c259f-116">2. példa: Címkék hozzáadása erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="c259f-116">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzureRmResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="c259f-117">Ebben a példában egy olyan állapotkódot ad meg, amely egy jóváhagyott értékkel rendelkezik, és egy FY2016 címkét tartalmaz egy meglévő címkéket tartalmazó erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="c259f-117">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="c259f-118">Mivel a megadott címkék felülírják a meglévő címkéket, a meglévő címkéket meg kell jeleníteni az új címkét tartalmazó gyűjteményben, vagy elveszíti őket.</span><span class="sxs-lookup"><span data-stu-id="c259f-118">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>

<span data-ttu-id="c259f-119">Az első parancs megkapja a ContosoRG erőforráscsoport értékét, és a dot metódus segítségével Kinyeri a címkék tulajdonság értékét.</span><span class="sxs-lookup"><span data-stu-id="c259f-119">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="c259f-120">A parancs a címkéket a $Tags változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c259f-120">The command stores the tags in the $Tags variable.</span></span>

<span data-ttu-id="c259f-121">A második parancs a címkéket a $Tags változóban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c259f-121">The second command gets the tags in the $Tags variable.</span></span>

<span data-ttu-id="c259f-122">A harmadik parancs a + = hozzárendelés-operátor segítségével felveszi az állapotot és a FY2016 a címkék sorába a $Tags változóban.</span><span class="sxs-lookup"><span data-stu-id="c259f-122">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>

<span data-ttu-id="c259f-123">A negyedik parancs a **set-AzureRmResourceGroup** *címke* paraméterével alkalmazza a címkéket a $Tags változóban a ContosoRG-erőforrás csoportba.</span><span class="sxs-lookup"><span data-stu-id="c259f-123">The fourth command uses the *Tag* parameter of **Set-AzureRmResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>

<span data-ttu-id="c259f-124">Az ötödik parancs beilleszti az összes, a ContosoRG-erőforráscsoporthoz alkalmazott címkét.</span><span class="sxs-lookup"><span data-stu-id="c259f-124">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="c259f-125">A kimenet azt mutatja, hogy az erőforráscsoport rendelkezik a részleg címkével, valamint a két új címkével, az állapottal és a FY2015.</span><span class="sxs-lookup"><span data-stu-id="c259f-125">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="c259f-126">3. példa: erőforráscsoport összes címkéjének törlése</span><span class="sxs-lookup"><span data-stu-id="c259f-126">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="c259f-127">Ez a parancs azt a *címkét* megadó paramétert adja meg, amely egy üres ujjlenyomat-tábla értékkel rendelkezik az összes címke törléséhez a ContosoRG-erőforráscsoport közül.</span><span class="sxs-lookup"><span data-stu-id="c259f-127">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="c259f-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c259f-128">PARAMETERS</span></span>

### <span data-ttu-id="c259f-129">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c259f-129">-ApiVersion</span></span>
<span data-ttu-id="c259f-130">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="c259f-130">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="c259f-131">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="c259f-131">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c259f-132">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="c259f-132">-Id</span></span>
<span data-ttu-id="c259f-133">A módosítani kívánt erőforráscsoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c259f-133">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the Id.
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c259f-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c259f-134">-Name</span></span>
<span data-ttu-id="c259f-135">A módosítani kívánt erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c259f-135">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the name.
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c259f-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="c259f-136">-Pre</span></span>
<span data-ttu-id="c259f-137">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="c259f-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c259f-138">-Címke</span><span class="sxs-lookup"><span data-stu-id="c259f-138">-Tag</span></span>
<span data-ttu-id="c259f-139">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="c259f-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c259f-140">Példa:</span><span class="sxs-lookup"><span data-stu-id="c259f-140">For example:</span></span>

<span data-ttu-id="c259f-141">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="c259f-141">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="c259f-142">A címke egy olyan név-érték páros, amelyet létrehozhat, és alkalmazhat az erőforrásokra és az erőforrás-csoportokra.</span><span class="sxs-lookup"><span data-stu-id="c259f-142">A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="c259f-143">Miután címkéket rendelt az erőforrásokhoz és csoportokhoz, a *címke* paramétert használhatja Get-AzureRmResource és a Get-AzureRmResourceGroup segítségével az erőforrások és a csoportok címkét adhat a név vagy a név és az érték megadásával.</span><span class="sxs-lookup"><span data-stu-id="c259f-143">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="c259f-144">Címkéket használhat az erőforrások (például részleg vagy költséghely) kategorizálásához, illetve az erőforrásokkal kapcsolatos megjegyzések és megjegyzések nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="c259f-144">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>

<span data-ttu-id="c259f-145">Címke hozzáadásához vagy módosításához az erőforráscsoport címkéjének gyűjteményét kell lecserélnie.</span><span class="sxs-lookup"><span data-stu-id="c259f-145">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="c259f-146">Ha törölni szeretne egy címkét, írja be az összes olyan címkét, amely az erőforráscsoport által használt összes címkét, a **Get-AzureRmResourceGroup** , kivéve a törölni kívánt címkét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c259f-146">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzureRmResourceGroup** , except for the tag you want to delete.</span></span> <span data-ttu-id="c259f-147">Ha az összes címkét törölni szeretné egy erőforráscsoport esetében, adjon meg egy üres kivonatoló táblát: `@{}` .</span><span class="sxs-lookup"><span data-stu-id="c259f-147">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c259f-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c259f-148">-DefaultProfile</span></span>
<span data-ttu-id="c259f-149">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c259f-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c259f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c259f-150">CommonParameters</span></span>
<span data-ttu-id="c259f-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c259f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c259f-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c259f-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c259f-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c259f-153">INPUTS</span></span>

### <span data-ttu-id="c259f-154">Nincs</span><span class="sxs-lookup"><span data-stu-id="c259f-154">None</span></span>

## <span data-ttu-id="c259f-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c259f-155">OUTPUTS</span></span>

### <span data-ttu-id="c259f-156">Microsoft. Azure. Command. Resources. models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c259f-156">Microsoft.Azure.Commands.Resources.Models.PSResourceGroup</span></span>

## <span data-ttu-id="c259f-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c259f-157">NOTES</span></span>

## <span data-ttu-id="c259f-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c259f-158">RELATED LINKS</span></span>

[<span data-ttu-id="c259f-159">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="c259f-159">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="c259f-160">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c259f-160">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="c259f-161">Új – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c259f-161">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="c259f-162">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c259f-162">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)
