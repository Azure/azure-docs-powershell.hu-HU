---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 125B6865-0022-4F88-BB0F-DDDDB2EDFF00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a1f1d033c3e8bae708310d12a1c4cb2b581bf80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015800"
---
# <span data-ttu-id="41eb5-101">Set-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="41eb5-101">Set-AzureNetworkSecurityRule</span></span>

## <span data-ttu-id="41eb5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="41eb5-103">Hálózatbiztonsági szabály hozzáadása vagy módosítása egy hálózati biztonsági csoportban</span><span class="sxs-lookup"><span data-stu-id="41eb5-103">Adds or modifies a network security rule in a network security group.</span></span>

## <span data-ttu-id="41eb5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41eb5-104">SYNTAX</span></span>

```
Set-AzureNetworkSecurityRule -Name <String> -Type <String> -Priority <Int32> -Action <String>
 -SourceAddressPrefix <String> -SourcePortRange <String> -DestinationAddressPrefix <String>
 -DestinationPortRange <String> -Protocol <String> -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="41eb5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="41eb5-105">DESCRIPTION</span></span>
<span data-ttu-id="41eb5-106">A **set-AzureNetworkSecurityRule** parancsmag az Azure Network biztonsági szabályait hozzáadja vagy módosítja egy hálózati biztonsági csoportban.</span><span class="sxs-lookup"><span data-stu-id="41eb5-106">The **Set-AzureNetworkSecurityRule** cmdlet adds or modifies an Azure network security rule in a network security group.</span></span>

## <span data-ttu-id="41eb5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="41eb5-107">EXAMPLES</span></span>

## <span data-ttu-id="41eb5-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41eb5-108">PARAMETERS</span></span>

### <span data-ttu-id="41eb5-109">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="41eb5-109">-Action</span></span>
<span data-ttu-id="41eb5-110">A hálózati biztonsági szabályokra vonatkozó műveleteket adja meg.</span><span class="sxs-lookup"><span data-stu-id="41eb5-110">Specifies the action for a network security rule.</span></span>
<span data-ttu-id="41eb5-111">Az érvényes értékek: Allow és deny.</span><span class="sxs-lookup"><span data-stu-id="41eb5-111">Valid values are: Allow and Deny.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eb5-112">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="41eb5-112">-DestinationAddressPrefix</span></span>
<span data-ttu-id="41eb5-113">A hálózati biztonsági szabálynak a cél IP-tartományának osztály nélküli tartományok közötti útválasztási (CIDR) címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41eb5-113">Specifies the Classless Interdomain Routing (CIDR) address of the destination IP range for the network security rule.</span></span>
<span data-ttu-id="41eb5-114">A csillag (\*) az IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="41eb5-114">An asterisk (\*) specifies any IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eb5-115">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="41eb5-115">-DestinationPortRange</span></span>
<span data-ttu-id="41eb5-116">A hálózat biztonsági szabályának célport-hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41eb5-116">Specifies a destination port range for the network security rule.</span></span>
<span data-ttu-id="41eb5-117">Az érvényes értékek 0 és 65535 közötti egész számok.</span><span class="sxs-lookup"><span data-stu-id="41eb5-117">Valid values consist of integers from 0 to 65535.</span></span>
<span data-ttu-id="41eb5-118">Megadhat egy egyedi értéket, vagy megadhat egy LowerNumber-HigherNumber.</span><span class="sxs-lookup"><span data-stu-id="41eb5-118">You can specify an individual value, or specify a range in the format LowerNumber-HigherNumber.</span></span>
<span data-ttu-id="41eb5-119">Egy kötőjel választja el a két értéket.</span><span class="sxs-lookup"><span data-stu-id="41eb5-119">A hyphen separates the two values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eb5-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="41eb5-120">-Name</span></span>
<span data-ttu-id="41eb5-121">A parancsmag által hozzáadott vagy módosított hálózati biztonsági szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41eb5-121">Specifies the name for the network security rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eb5-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="41eb5-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="41eb5-123">Azt a hálózati biztonsági csoportot adja meg, amelyre a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="41eb5-123">Specifies the network security group that this cmdlet modifies.</span></span>
<span data-ttu-id="41eb5-124">**INetworkSecurityGroup** objektum beolvasásához használja az Get-AzureNetworkSecurityGroup parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="41eb5-124">To obtain an **INetworkSecurityGroup** object, use the Get-AzureNetworkSecurityGroup cmdlet.</span></span>

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41eb5-125">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="41eb5-125">-Priority</span></span>
<span data-ttu-id="41eb5-126">A hálózati biztonsági szabály prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="41eb5-126">Specifies the priority for the network security rule.</span></span>
<span data-ttu-id="41eb5-127">Az érvényes értékek a következők: 100-től 4096-ig terjedő egész számok.</span><span class="sxs-lookup"><span data-stu-id="41eb5-127">Valid values are: integers from 100 to 4096.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eb5-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="41eb5-128">-Profile</span></span>
<span data-ttu-id="41eb5-129">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="41eb5-129">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="41eb5-130">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="41eb5-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eb5-131">-Protocol</span><span class="sxs-lookup"><span data-stu-id="41eb5-131">-Protocol</span></span>
<span data-ttu-id="41eb5-132">A hálózati biztonsági szabály protokollját adja meg.</span><span class="sxs-lookup"><span data-stu-id="41eb5-132">Specifies the protocol for the network security rule.</span></span>
<span data-ttu-id="41eb5-133">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="41eb5-133">Valid values are:</span></span> 

- <span data-ttu-id="41eb5-134">TCP</span><span class="sxs-lookup"><span data-stu-id="41eb5-134">TCP</span></span> 
- <span data-ttu-id="41eb5-135">UDP</span><span class="sxs-lookup"><span data-stu-id="41eb5-135">UDP</span></span> 
- *

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eb5-136">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="41eb5-136">-SourceAddressPrefix</span></span>
<span data-ttu-id="41eb5-137">A hálózati biztonsági szabály forrás IP-CIDR címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41eb5-137">Specifies the CIDR address of the source IP range for the network security rule.</span></span>
<span data-ttu-id="41eb5-138">A csillag (\*) az IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="41eb5-138">An asterisk (\*) specifies any IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eb5-139">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="41eb5-139">-SourcePortRange</span></span>
<span data-ttu-id="41eb5-140">Megadja a hálózati biztonsági szabály forrásport-hatókörét.</span><span class="sxs-lookup"><span data-stu-id="41eb5-140">Specifies a source port range for the network security rule.</span></span>
<span data-ttu-id="41eb5-141">Az érvényes értékek 0 és 65535 közötti egész számok.</span><span class="sxs-lookup"><span data-stu-id="41eb5-141">Valid values consist of integers from 0 to 65535.</span></span>
<span data-ttu-id="41eb5-142">Megadhat egy egyedi értéket, vagy megadhat egy LowerNumber-HigherNumber.</span><span class="sxs-lookup"><span data-stu-id="41eb5-142">You can specify an individual value, or specify a range in the format LowerNumber-HigherNumber.</span></span>
<span data-ttu-id="41eb5-143">Egy kötőjel választja el a két értéket.</span><span class="sxs-lookup"><span data-stu-id="41eb5-143">A hyphen separates the two values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eb5-144">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="41eb5-144">-Type</span></span>
<span data-ttu-id="41eb5-145">A hálózati biztonsági szabályhoz tartozó kapcsolat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="41eb5-145">Specifies the type of connection for the network security rule.</span></span>
<span data-ttu-id="41eb5-146">Érvényes értékek: bejövő és kimenő.</span><span class="sxs-lookup"><span data-stu-id="41eb5-146">Valid values are: Inbound and Outbound.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eb5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41eb5-147">CommonParameters</span></span>
<span data-ttu-id="41eb5-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41eb5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41eb5-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41eb5-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41eb5-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41eb5-150">INPUTS</span></span>

## <span data-ttu-id="41eb5-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41eb5-151">OUTPUTS</span></span>

## <span data-ttu-id="41eb5-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41eb5-152">NOTES</span></span>

## <span data-ttu-id="41eb5-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41eb5-153">RELATED LINKS</span></span>

[<span data-ttu-id="41eb5-154">Remove-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="41eb5-154">Remove-AzureNetworkSecurityRule</span></span>](./Remove-AzureNetworkSecurityRule.md)


