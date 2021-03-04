---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: f344c3cd08fb717d1229fb0abb4386c8a2d39d5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941441"
---
# <span data-ttu-id="2b0bf-101">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2b0bf-101">Set-AzResourceGroup</span></span>

## <span data-ttu-id="2b0bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b0bf-102">SYNOPSIS</span></span>
<span data-ttu-id="2b0bf-103">Módosít egy erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-103">Modifies a resource group.</span></span>

## <span data-ttu-id="2b0bf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2b0bf-104">SYNTAX</span></span>

### <span data-ttu-id="2b0bf-105">SetByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2b0bf-105">SetByResourceGroupName (Default)</span></span>
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b0bf-106">SetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="2b0bf-106">SetByResourceGroupId</span></span>
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b0bf-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2b0bf-107">DESCRIPTION</span></span>
<span data-ttu-id="2b0bf-108">A **Set-AzResourceGroup** parancsmag módosítja egy erőforráscsoport tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-108">The **Set-AzResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="2b0bf-109">Ezzel a parancsmagtal hozzáadhatja, módosíthatja vagy törölheti az erőforráscsoportokra alkalmazott Azure-címkéket.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-109">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="2b0bf-110">Adja meg *a Name paramétert* az erőforráscsoport azonosításához, a *Címke* paramétert pedig a címkék módosításához.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-110">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>
<span data-ttu-id="2b0bf-111">Ezzel a parancsmagtal nem módosíthatja egy erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-111">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="2b0bf-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2b0bf-112">EXAMPLES</span></span>

### <span data-ttu-id="2b0bf-113">1. példa: Címke alkalmazása erőforráscsoportra</span><span class="sxs-lookup"><span data-stu-id="2b0bf-113">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="2b0bf-114">Ez a parancs egy it-értékkel megadott Részleg címkét alkalmaz egy olyan erőforráscsoportra, amely nem rendelkezik meglévő címkékkel.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-114">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="2b0bf-115">2. példa: Címkék hozzáadása erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="2b0bf-115">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="2b0bf-116">Ebben a példában egy "Jóváhagyva" értékkel és egy 2016-os FY2016-os címkével egy meglévő címkéket kezelő erőforráscsoporthoz ad hozzá egy állapotcímkét.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-116">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="2b0bf-117">Mivel a megadott címkék lecserélik a meglévő címkéket, a meglévő címkéket fel kell foglalnia az új címkegyűjteménybe, különben elvesznek.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-117">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>
<span data-ttu-id="2b0bf-118">Az első parancs a ContosoRG erőforráscsoportot kapja meg, és a pont módszerrel be tudja szerezni a Címkék tulajdonság értékét.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-118">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="2b0bf-119">A parancs a címkéket a $Tags tárolja.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-119">The command stores the tags in the $Tags variable.</span></span>
<span data-ttu-id="2b0bf-120">A második parancs megkapja a címkéket a $Tags változóban.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-120">The second command gets the tags in the $Tags variable.</span></span>
<span data-ttu-id="2b0bf-121">A harmadik parancs a += hozzárendelési operátorral adja hozzá az állapot- és 2016-os címkéket a címketömbhöz a $Tags változóban.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-121">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>
<span data-ttu-id="2b0bf-122">A negyedik parancs *a* **Set-AzResourceGroup** Címke paraméterével alkalmazza a $Tags címkéit a ContosoRG erőforráscsoportra.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-122">The fourth command uses the *Tag* parameter of **Set-AzResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>
<span data-ttu-id="2b0bf-123">Az ötödik parancs a ContosoRG erőforráscsoportra alkalmazott összes címkét begyakorlja.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-123">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="2b0bf-124">A kimenet azt mutatja, hogy az erőforráscsoport részlegcímkével és a két új címkével (Állapot és Y2015) rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-124">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="2b0bf-125">3. példa: Erőforráscsoport összes címkéének törlése</span><span class="sxs-lookup"><span data-stu-id="2b0bf-125">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="2b0bf-126">Ez a parancs a *Címke* paramétert adja meg egy üres kivonattábla-értékkel, amely törli az összes címkét a ContosoRG erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-126">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="2b0bf-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b0bf-127">PARAMETERS</span></span>

### <span data-ttu-id="2b0bf-128">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2b0bf-128">-ApiVersion</span></span>
<span data-ttu-id="2b0bf-129">Az erőforrásszolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-129">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="2b0bf-130">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-130">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="2b0bf-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b0bf-131">-DefaultProfile</span></span>
<span data-ttu-id="2b0bf-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2b0bf-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b0bf-133">-Id</span><span class="sxs-lookup"><span data-stu-id="2b0bf-133">-Id</span></span>
<span data-ttu-id="2b0bf-134">A módosítani szükséges erőforráscsoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-134">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b0bf-135">-Name</span><span class="sxs-lookup"><span data-stu-id="2b0bf-135">-Name</span></span>
<span data-ttu-id="2b0bf-136">A módosítani szükséges erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-136">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b0bf-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="2b0bf-137">-Pre</span></span>
<span data-ttu-id="2b0bf-138">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2b0bf-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="2b0bf-139">-Tag</span></span>
<span data-ttu-id="2b0bf-140">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2b0bf-141">Például: @{key0="érték0";key1=$null;key2="érték2"} A címke egy névérték-pár, amely létrehozható és alkalmazható erőforrásokra és erőforráscsoportokra.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-141">For example: @{key0="value0";key1=$null;key2="value2"} A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="2b0bf-142">Miután címkéket rendel erőforrásokhoz és csoportokhoz, a Get-AzResource és a Get-AzResourceGroup címke paraméterével kereshet erőforrásokat és csoportokat címkenév, név és érték alapján. </span><span class="sxs-lookup"><span data-stu-id="2b0bf-142">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="2b0bf-143">Címkékkel kategorizálhatja az erőforrásokat, például részlegek vagy költségközpontok szerint, illetve nyomon követheti az erőforrásokkal kapcsolatos jegyzeteket vagy megjegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-143">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="2b0bf-144">Címke hozzáadásához vagy cseréjéhez le kell cserélnie az erőforráscsoport címkéinek gyűjteményét.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="2b0bf-145">Címke törléséhez írjon be egy olyan kivonattáblát, amely az erőforráscsoportra jelenleg alkalmazott összes címkét tartalmazza a **Get-AzResourceGroup** csoportból , kivéve a törölni kívánt címkét.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-145">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzResourceGroup**, except for the tag you want to delete.</span></span> <span data-ttu-id="2b0bf-146">Ha egy erőforráscsoport összes címkéét törölni szeretné, adjon meg egy üres kivonattáblát: `@{}` .</span><span class="sxs-lookup"><span data-stu-id="2b0bf-146">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

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

### <span data-ttu-id="2b0bf-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b0bf-147">CommonParameters</span></span>
<span data-ttu-id="2b0bf-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b0bf-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b0bf-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b0bf-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b0bf-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b0bf-150">INPUTS</span></span>

### <span data-ttu-id="2b0bf-151">System.String</span><span class="sxs-lookup"><span data-stu-id="2b0bf-151">System.String</span></span>

### <span data-ttu-id="2b0bf-152">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2b0bf-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2b0bf-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b0bf-153">OUTPUTS</span></span>

### <span data-ttu-id="2b0bf-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2b0bf-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="2b0bf-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2b0bf-155">NOTES</span></span>

## <span data-ttu-id="2b0bf-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b0bf-156">RELATED LINKS</span></span>

[<span data-ttu-id="2b0bf-157">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="2b0bf-157">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="2b0bf-158">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2b0bf-158">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="2b0bf-159">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2b0bf-159">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="2b0bf-160">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2b0bf-160">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)
