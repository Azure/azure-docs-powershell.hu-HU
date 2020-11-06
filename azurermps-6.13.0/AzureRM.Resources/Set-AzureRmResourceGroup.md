---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
ms.openlocfilehash: 4ba57d1f8e1abe8c506f1bcd6625a7a90551f164
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503392"
---
# <span data-ttu-id="fe2cb-101">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fe2cb-101">Set-AzureRmResourceGroup</span></span>

## <span data-ttu-id="fe2cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe2cb-102">SYNOPSIS</span></span>
<span data-ttu-id="fe2cb-103">Egy erőforráscsoport módosítása</span><span class="sxs-lookup"><span data-stu-id="fe2cb-103">Modifies a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe2cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe2cb-104">SYNTAX</span></span>

### <span data-ttu-id="fe2cb-105">SetByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fe2cb-105">SetByResourceGroupName (Default)</span></span>
```
Set-AzureRmResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe2cb-106">SetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="fe2cb-106">SetByResourceGroupId</span></span>
```
Set-AzureRmResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe2cb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe2cb-107">DESCRIPTION</span></span>
<span data-ttu-id="fe2cb-108">A **set-AzureRmResourceGroup** parancsmag egy erőforráscsoport tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-108">The **Set-AzureRmResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="fe2cb-109">Ezzel a parancsmaggal megadhatja, módosíthatja vagy törölheti az erőforrás-csoportokra alkalmazott Azure-címkéket.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-109">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="fe2cb-110">Adja meg a *Name (név* ) paramétert az erőforráscsoport meghatározásához, illetve a *címke* paramétert a címkék módosításához.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-110">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>
<span data-ttu-id="fe2cb-111">Ez a parancsmag nem használható az erőforráscsoport nevének módosítására.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-111">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="fe2cb-112">Példák</span><span class="sxs-lookup"><span data-stu-id="fe2cb-112">EXAMPLES</span></span>

### <span data-ttu-id="fe2cb-113">1. példa: címke alkalmazása erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="fe2cb-113">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="fe2cb-114">Ez a parancs egy olyan részleg címkét alkalmaz, amelynek az értéke egy olyan erőforráscsoport, amely nem tartalmaz meglévő címkéket.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-114">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="fe2cb-115">2. példa: Címkék hozzáadása erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="fe2cb-115">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzureRmResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="fe2cb-116">Ebben a példában egy olyan állapotkódot ad meg, amely egy jóváhagyott értékkel rendelkezik, és egy FY2016 címkét tartalmaz egy meglévő címkéket tartalmazó erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-116">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="fe2cb-117">Mivel a megadott címkék felülírják a meglévő címkéket, a meglévő címkéket meg kell jeleníteni az új címkét tartalmazó gyűjteményben, vagy elveszíti őket.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-117">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>
<span data-ttu-id="fe2cb-118">Az első parancs megkapja a ContosoRG erőforráscsoport értékét, és a dot metódus segítségével Kinyeri a címkék tulajdonság értékét.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-118">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="fe2cb-119">A parancs a címkéket a $Tags változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-119">The command stores the tags in the $Tags variable.</span></span>
<span data-ttu-id="fe2cb-120">A második parancs a címkéket a $Tags változóban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-120">The second command gets the tags in the $Tags variable.</span></span>
<span data-ttu-id="fe2cb-121">A harmadik parancs a + = hozzárendelés-operátor segítségével felveszi az állapotot és a FY2016 a címkék sorába a $Tags változóban.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-121">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>
<span data-ttu-id="fe2cb-122">A negyedik parancs a **set-AzureRmResourceGroup** *címke* paraméterével alkalmazza a címkéket a $Tags változóban a ContosoRG-erőforrás csoportba.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-122">The fourth command uses the *Tag* parameter of **Set-AzureRmResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>
<span data-ttu-id="fe2cb-123">Az ötödik parancs beilleszti az összes, a ContosoRG-erőforráscsoporthoz alkalmazott címkét.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-123">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="fe2cb-124">A kimenet azt mutatja, hogy az erőforráscsoport rendelkezik a részleg címkével, valamint a két új címkével, az állapottal és a FY2015.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-124">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="fe2cb-125">3. példa: erőforráscsoport összes címkéjének törlése</span><span class="sxs-lookup"><span data-stu-id="fe2cb-125">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="fe2cb-126">Ez a parancs azt a *címkét* megadó paramétert adja meg, amely egy üres ujjlenyomat-tábla értékkel rendelkezik az összes címke törléséhez a ContosoRG-erőforráscsoport közül.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-126">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="fe2cb-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe2cb-127">PARAMETERS</span></span>

### <span data-ttu-id="fe2cb-128">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fe2cb-128">-ApiVersion</span></span>
<span data-ttu-id="fe2cb-129">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-129">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="fe2cb-130">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-130">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="fe2cb-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe2cb-131">-DefaultProfile</span></span>
<span data-ttu-id="fe2cb-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fe2cb-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe2cb-133">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="fe2cb-133">-Id</span></span>
<span data-ttu-id="fe2cb-134">A módosítani kívánt erőforráscsoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-134">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe2cb-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fe2cb-135">-Name</span></span>
<span data-ttu-id="fe2cb-136">A módosítani kívánt erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-136">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2cb-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="fe2cb-137">-Pre</span></span>
<span data-ttu-id="fe2cb-138">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fe2cb-139">-Címke</span><span class="sxs-lookup"><span data-stu-id="fe2cb-139">-Tag</span></span>
<span data-ttu-id="fe2cb-140">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fe2cb-141">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"} A címke egy olyan név-érték páros, amelyet létrehozhat, és alkalmazhat az erőforrásokra és az erőforrás-csoportokra.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-141">For example: @{key0="value0";key1=$null;key2="value2"} A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="fe2cb-142">Miután címkéket rendelt az erőforrásokhoz és csoportokhoz, a *címke* paramétert használhatja Get-AzureRmResource és a Get-AzureRmResourceGroup segítségével az erőforrások és a csoportok címkét adhat a név vagy a név és az érték megadásával.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-142">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="fe2cb-143">Címkéket használhat az erőforrások (például részleg vagy költséghely) kategorizálásához, illetve az erőforrásokkal kapcsolatos megjegyzések és megjegyzések nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-143">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="fe2cb-144">Címke hozzáadásához vagy módosításához az erőforráscsoport címkéjének gyűjteményét kell lecserélnie.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="fe2cb-145">Ha törölni szeretne egy címkét, írja be az összes olyan címkét, amely az erőforráscsoport által használt összes címkét, a **Get-AzureRmResourceGroup** , kivéve a törölni kívánt címkét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fe2cb-145">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzureRmResourceGroup** , except for the tag you want to delete.</span></span> <span data-ttu-id="fe2cb-146">Ha az összes címkét törölni szeretné egy erőforráscsoport esetében, adjon meg egy üres kivonatoló táblát: `@{}` .</span><span class="sxs-lookup"><span data-stu-id="fe2cb-146">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

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

### <span data-ttu-id="fe2cb-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe2cb-147">CommonParameters</span></span>
<span data-ttu-id="fe2cb-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe2cb-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe2cb-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe2cb-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe2cb-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe2cb-150">INPUTS</span></span>

### <span data-ttu-id="fe2cb-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="fe2cb-151">None</span></span>

## <span data-ttu-id="fe2cb-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe2cb-152">OUTPUTS</span></span>

### <span data-ttu-id="fe2cb-153">Microsoft. Azure. Command. Resources. models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fe2cb-153">Microsoft.Azure.Commands.Resources.Models.PSResourceGroup</span></span>

## <span data-ttu-id="fe2cb-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe2cb-154">NOTES</span></span>

## <span data-ttu-id="fe2cb-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe2cb-155">RELATED LINKS</span></span>

[<span data-ttu-id="fe2cb-156">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fe2cb-156">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="fe2cb-157">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fe2cb-157">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="fe2cb-158">Új – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fe2cb-158">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="fe2cb-159">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fe2cb-159">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)