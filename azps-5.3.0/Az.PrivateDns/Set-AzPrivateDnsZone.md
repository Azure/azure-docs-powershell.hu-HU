---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: 06b8a8bd7027b95d7f51e186b0184707ffd296a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466669"
---
# <span data-ttu-id="9a1d0-101">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="9a1d0-101">Set-AzPrivateDnsZone</span></span>

## <span data-ttu-id="9a1d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a1d0-102">SYNOPSIS</span></span>
<span data-ttu-id="9a1d0-103">Frissíti a privát DNS-zónát egy erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="9a1d0-103">Updates a Private DNS zone from a resource group.</span></span>

## <span data-ttu-id="9a1d0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9a1d0-104">SYNTAX</span></span>

### <span data-ttu-id="9a1d0-105">Mezők (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9a1d0-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a1d0-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a1d0-106">ResourceId</span></span>
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a1d0-107">Objektum</span><span class="sxs-lookup"><span data-stu-id="9a1d0-107">Object</span></span>
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a1d0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9a1d0-108">DESCRIPTION</span></span>
<span data-ttu-id="9a1d0-109">A **Set-AzPrivateDnsZone** parancsmag véglegesen frissíti a dns-zónát egy adott erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="9a1d0-109">The **Set-AzPrivateDnsZone** cmdlet permanently updates a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="9a1d0-110">A **PrivateDnsZone-objektumokat** a *PrivateZone* paraméterrel vagy a folyamat műveleti jelével, illetve a *Name* and *ResourceGroupName* paraméter megadásával is átadhatja.</span><span class="sxs-lookup"><span data-stu-id="9a1d0-110">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="9a1d0-111">A Confirm paraméter és a Windows PowerShell $ConfirmPreference szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="9a1d0-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="9a1d0-112">Amikor a zónát **egy PrivateDnsZone-objektummal** adja  meg (amely a folyamaton vagy a Zóna paraméteren keresztül lett átadva), a zóna nem frissül, ha módosult az Azure DNS-ben a helyi **PrivateDnsZone** objektum beolvasása óta (csak a DNS-zóna erőforrásszámán végrehajtott műveletek változásként, a rekordkészletek műveletei a zónán belül nem).</span><span class="sxs-lookup"><span data-stu-id="9a1d0-112">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="9a1d0-113">Ez védelmet nyújt a párhuzamos zónaváltozások számára.</span><span class="sxs-lookup"><span data-stu-id="9a1d0-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="9a1d0-114">Ez elrejthető a  Felülírás paraméter használatával, amely a egyidejűleg végrehajtott módosításoktól függetlenül frissíti a zónát.</span><span class="sxs-lookup"><span data-stu-id="9a1d0-114">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="9a1d0-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9a1d0-115">EXAMPLES</span></span>

### <span data-ttu-id="9a1d0-116">1. példa: Privát zóna frissítése</span><span class="sxs-lookup"><span data-stu-id="9a1d0-116">Example 1: Updates a private zone</span></span>
```
PS C:\>Set-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup" -Tag @{tag1="value1";tag2="value2"}


This command updates the zone named myzone.com from the resource group named MyResourceGroup with the tags provided. Use Get-AzPrivateDnsZone to retrieve the updated zone. Updated zone would look something like this:

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {tag1="value1";tag2="value2"}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="9a1d0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a1d0-117">PARAMETERS</span></span>

### <span data-ttu-id="9a1d0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a1d0-118">-DefaultProfile</span></span>
<span data-ttu-id="9a1d0-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9a1d0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a1d0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9a1d0-120">-Name</span></span>
<span data-ttu-id="9a1d0-121">A parancsmag által frissülő privát DNS-zóna neve.</span><span class="sxs-lookup"><span data-stu-id="9a1d0-121">Specifies the name of the Private DNS zone that this cmdlet updates.</span></span>
<span data-ttu-id="9a1d0-122">Az *ResourceGroupName* paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="9a1d0-122">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="9a1d0-123">Másik lehetőségként megadhatja a privát DNS-zónát a *Zone paraméter* használatával.</span><span class="sxs-lookup"><span data-stu-id="9a1d0-123">Alternatively, you can specify the private DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="9a1d0-124">-Felülírás</span><span class="sxs-lookup"><span data-stu-id="9a1d0-124">-Overwrite</span></span>
<span data-ttu-id="9a1d0-125">Amikor a zónát **egy PrivateDnsZone-objektummal** adja  meg (amely a folyamaton vagy a Zóna paraméteren keresztül lett átadva), a zóna nem frissül, ha módosult az Azure DNS-ben a helyi **DnsZone-objektum** beolvasása óta (csak a DNS-zóna erőforrásának módosításain végrehajtott műveletek, a zónán belüli rekordkészletek műveletei nem).</span><span class="sxs-lookup"><span data-stu-id="9a1d0-125">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="9a1d0-126">Ez védelmet nyújt a párhuzamos zónaváltozások számára.</span><span class="sxs-lookup"><span data-stu-id="9a1d0-126">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="9a1d0-127">Ez elrejthető a  Felülírás paraméter használatával, amely a egyidejűleg végrehajtott módosításoktól függetlenül frissíti a zónát.</span><span class="sxs-lookup"><span data-stu-id="9a1d0-127">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="9a1d0-128">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="9a1d0-128">-PrivateZone</span></span>
<span data-ttu-id="9a1d0-129">A beállított zónaobjektum.</span><span class="sxs-lookup"><span data-stu-id="9a1d0-129">The zone object to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1d0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a1d0-130">-ResourceGroupName</span></span>
<span data-ttu-id="9a1d0-131">Annak az erőforráscsoportnak a nevét adja meg, amely a frissíteni kívánt zónát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9a1d0-131">Specifies the name of the resource group that contains the zone to be updated.</span></span>
<span data-ttu-id="9a1d0-132">A *ZoneName* paramétert is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="9a1d0-132">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="9a1d0-133">Másik lehetőségként megadhatja a privát DNS-zónát egy **DnsZone-objektum** használatával, amely vagy a folyamaton, vagy a Zone paraméteren *keresztül adható* meg.</span><span class="sxs-lookup"><span data-stu-id="9a1d0-133">Alternatively, you can specify the private DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="9a1d0-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a1d0-134">-ResourceId</span></span>
<span data-ttu-id="9a1d0-135">Private DNS Zone ResourceID.</span><span class="sxs-lookup"><span data-stu-id="9a1d0-135">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="9a1d0-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="9a1d0-136">-Tag</span></span>
<span data-ttu-id="9a1d0-137">A hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="9a1d0-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="9a1d0-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a1d0-138">-Confirm</span></span>
<span data-ttu-id="9a1d0-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9a1d0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a1d0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a1d0-140">-WhatIf</span></span>
<span data-ttu-id="9a1d0-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9a1d0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a1d0-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9a1d0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a1d0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a1d0-143">CommonParameters</span></span>
<span data-ttu-id="9a1d0-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a1d0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a1d0-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a1d0-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a1d0-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a1d0-146">INPUTS</span></span>

### <span data-ttu-id="9a1d0-147">System.String</span><span class="sxs-lookup"><span data-stu-id="9a1d0-147">System.String</span></span>

### <span data-ttu-id="9a1d0-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="9a1d0-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="9a1d0-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a1d0-149">OUTPUTS</span></span>

### <span data-ttu-id="9a1d0-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="9a1d0-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="9a1d0-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9a1d0-151">NOTES</span></span>

## <span data-ttu-id="9a1d0-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a1d0-152">RELATED LINKS</span></span>

[<span data-ttu-id="9a1d0-153">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="9a1d0-153">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="9a1d0-154">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="9a1d0-154">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="9a1d0-155">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="9a1d0-155">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
