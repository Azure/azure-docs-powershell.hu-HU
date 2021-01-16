---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 3ffcc30dc0291be06c27ee53ee0ee7ea14f3e2c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341778"
---
# <span data-ttu-id="2ac63-101">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="2ac63-101">Set-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="2ac63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ac63-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac63-103">Egy privát zónához és egy erőforráscsoporthoz társított virtuális hálózati hivatkozást hoz létre/hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2ac63-103">Updates/Sets a virtual network link associated with a private zone and a resource group.</span></span>

## <span data-ttu-id="2ac63-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2ac63-104">SYNTAX</span></span>

### <span data-ttu-id="2ac63-105">Mezők (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2ac63-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ac63-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="2ac63-106">Object</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ac63-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ac63-107">ResourceId</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ac63-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2ac63-108">DESCRIPTION</span></span>
<span data-ttu-id="2ac63-109">A **Set-AzPrivateDnsVirtualNetworkLink** parancsmag frissíti a megadott erőforráscsoport zónájára mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="2ac63-109">The **Set-AzPrivateDnsVirtualNetworkLink** cmdlet updates a link associated with a zone from a specified resource group.</span></span>
<span data-ttu-id="2ac63-110">A **PSPrivateDnsVirtualNetworkLink** objektum a  Csatolás paraméterrel vagy a folyamat műveleti jelével adható át, vagy másik lehetőségként megadhatja a *Name* *ZoneName* és *az ResourceGroupName* paramétert.</span><span class="sxs-lookup"><span data-stu-id="2ac63-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="2ac63-111">A Confirm paraméter és a Windows PowerShell $ConfirmPreference szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="2ac63-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="2ac63-112">Amikor a zónát **PSPrivateDnsVirtualNetworkLink** objektummal adja meg  (a folyamaton vagy a Hivatkozás paraméteren keresztül adja át), a csatolás nem frissül, ha az Azure DNS-ben módosult a helyi **PSPrivateDnsVirtualNetworkLink** objektum lekérése óta.</span><span class="sxs-lookup"><span data-stu-id="2ac63-112">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not updated if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="2ac63-113">Ez védelmet nyújt az egyidejű hivatkozásváltozások számára.</span><span class="sxs-lookup"><span data-stu-id="2ac63-113">This provides protection for concurrent link changes.</span></span> <span data-ttu-id="2ac63-114">Ez elrejthető a  Felülírás paraméter használatával, amely a párhuzamos módosításoktól függetlenül frissíti a hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="2ac63-114">This can be suppressed using the *Overwrite* parameter, which updates the link regardless of concurrent changes.</span></span>

## <span data-ttu-id="2ac63-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2ac63-115">EXAMPLES</span></span>

### <span data-ttu-id="2ac63-116">1. példa: Hivatkozás beállítása</span><span class="sxs-lookup"><span data-stu-id="2ac63-116">Example 1: Set a link</span></span>
```
PS C:\>Set-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -Tag @{} -IsRegistrationEnabled $true

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="2ac63-117">Ez a parancs Az IsRegistrationEnabled érték igazra van halmaza a MyResourceGroup nevű erőforráscsoport myzone.com nevű zónához csatolva.</span><span class="sxs-lookup"><span data-stu-id="2ac63-117">This command sets IsRegistrationEnabled to True for the link named mylink, linked to zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="2ac63-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ac63-118">PARAMETERS</span></span>

### <span data-ttu-id="2ac63-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac63-119">-DefaultProfile</span></span>
<span data-ttu-id="2ac63-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2ac63-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ac63-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ac63-121">-InputObject</span></span>
<span data-ttu-id="2ac63-122">A beállítani szükséges virtuális hálózati csatolási objektum.</span><span class="sxs-lookup"><span data-stu-id="2ac63-122">The virtual network link object to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac63-123">-IsRegistrationEnabled</span><span class="sxs-lookup"><span data-stu-id="2ac63-123">-IsRegistrationEnabled</span></span>
<span data-ttu-id="2ac63-124">Logikai érték, amely azt jelzi, hogy a virtuális hálózati kapcsolaton engedélyezve van-e a regisztráció.</span><span class="sxs-lookup"><span data-stu-id="2ac63-124">Boolean that represents if registration is enabled on the virtual network link.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac63-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2ac63-125">-Name</span></span>
<span data-ttu-id="2ac63-126">A parancsmag által eltávolított hivatkozás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ac63-126">Specifies the name of the link that this cmdlet removes.</span></span>
<span data-ttu-id="2ac63-127">Az *ResourceGroupName* és *a ZoneName* paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="2ac63-127">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="2ac63-128">Másik lehetőségként megadhatja a privát DNS-hivatkozást a hivatkozás *paraméterrel.*</span><span class="sxs-lookup"><span data-stu-id="2ac63-128">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac63-129">-Felülírás</span><span class="sxs-lookup"><span data-stu-id="2ac63-129">-Overwrite</span></span>
<span data-ttu-id="2ac63-130">Ha **PSPrivateDnsVirtualNetworkLink** objektummal adja meg a hivatkozást  (amely a folyamaton vagy a Csatolás paraméteren keresztül lett átadva), a csatolás nem törlődik, ha az Azure DNS-ben módosult a helyi **PSPrivateDnsVirtualNetworkLink** objektum lekérése óta.</span><span class="sxs-lookup"><span data-stu-id="2ac63-130">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="2ac63-131">Ez védelmet nyújt az egyidejű hivatkozásváltozások számára.</span><span class="sxs-lookup"><span data-stu-id="2ac63-131">This provides protection for concurrent link changes.</span></span>
<span data-ttu-id="2ac63-132">Ez elrejthető a  Felülírás paraméter használatával, amely törli a hivatkozást, függetlenül az egyidejű módosításoktól.</span><span class="sxs-lookup"><span data-stu-id="2ac63-132">This can be suppressed using the *Overwrite* parameter, which deletes the link regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac63-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ac63-133">-ResourceGroupName</span></span>
<span data-ttu-id="2ac63-134">Annak az erőforráscsoportnak a nevét adja meg, amely az eltávolítható hivatkozást tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2ac63-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="2ac63-135">A *ZoneName* és a *Name paramétert is meg kell* adnia.</span><span class="sxs-lookup"><span data-stu-id="2ac63-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="2ac63-136">Másik lehetőségként megadhatja a virtuális hálózati kapcsolatot egy **PSPrivateDnsVirtualNetworkLink** objektummal, amely a folyamaton vagy a Csatolás paraméteren keresztül *áthalad.*</span><span class="sxs-lookup"><span data-stu-id="2ac63-136">Alternatively, you can specify the virtual network link using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac63-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ac63-137">-ResourceId</span></span>
<span data-ttu-id="2ac63-138">Private DNS Zone ResourceID.</span><span class="sxs-lookup"><span data-stu-id="2ac63-138">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac63-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="2ac63-139">-Tag</span></span>
<span data-ttu-id="2ac63-140">A hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="2ac63-140">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac63-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="2ac63-141">-ZoneName</span></span>
<span data-ttu-id="2ac63-142">A parancsmag által eltávolított DNS-zóna neve.</span><span class="sxs-lookup"><span data-stu-id="2ac63-142">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="2ac63-143">A Name and  *ResourceGroupName* paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="2ac63-143">You must also specify the *Name* and *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="2ac63-144">Másik lehetőségként megadhatja a privát DNS-hivatkozást a hivatkozás *paraméterrel.*</span><span class="sxs-lookup"><span data-stu-id="2ac63-144">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac63-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ac63-145">-Confirm</span></span>
<span data-ttu-id="2ac63-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2ac63-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac63-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ac63-147">-WhatIf</span></span>
<span data-ttu-id="2ac63-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2ac63-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ac63-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2ac63-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac63-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac63-150">CommonParameters</span></span>
<span data-ttu-id="2ac63-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ac63-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac63-152">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ac63-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac63-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ac63-153">INPUTS</span></span>

### <span data-ttu-id="2ac63-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="2ac63-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="2ac63-155">System.String</span><span class="sxs-lookup"><span data-stu-id="2ac63-155">System.String</span></span>

## <span data-ttu-id="2ac63-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ac63-156">OUTPUTS</span></span>

### <span data-ttu-id="2ac63-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="2ac63-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="2ac63-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2ac63-158">NOTES</span></span>

## <span data-ttu-id="2ac63-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ac63-159">RELATED LINKS</span></span>

[<span data-ttu-id="2ac63-160">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="2ac63-160">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="2ac63-161">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="2ac63-161">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="2ac63-162">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="2ac63-162">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
