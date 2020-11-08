---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BABA5142-541F-40C8-AFF5-20E4283BE147
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a718e2f675b4a5e204610a2d4f1fb1aac4c5478
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016150"
---
# <span data-ttu-id="6b7cb-101">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="6b7cb-101">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>

## <span data-ttu-id="6b7cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b7cb-102">SYNOPSIS</span></span>
<span data-ttu-id="6b7cb-103">A hálózat biztonsági csoportjának kihagyása egy alhálózatról.</span><span class="sxs-lookup"><span data-stu-id="6b7cb-103">Dissociates a network security group from a subnet.</span></span>

## <span data-ttu-id="6b7cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b7cb-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroupFromSubnet -Name <String> -VirtualNetworkName <String> -SubnetName <String>
 [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6b7cb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b7cb-105">DESCRIPTION</span></span>
<span data-ttu-id="6b7cb-106">A **Remove-AzureNetworkSecurityGroupFromSubnet** parancsmag egy alhálózatról egy Azure-hálózat biztonsági csoportját elhatárolja.</span><span class="sxs-lookup"><span data-stu-id="6b7cb-106">The **Remove-AzureNetworkSecurityGroupFromSubnet** cmdlet dissociates an Azure network security group from a subnet.</span></span>

## <span data-ttu-id="6b7cb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6b7cb-107">EXAMPLES</span></span>

## <span data-ttu-id="6b7cb-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b7cb-108">PARAMETERS</span></span>

### <span data-ttu-id="6b7cb-109">-Force</span><span class="sxs-lookup"><span data-stu-id="6b7cb-109">-Force</span></span>
<span data-ttu-id="6b7cb-110">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="6b7cb-110">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b7cb-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6b7cb-111">-Name</span></span>
<span data-ttu-id="6b7cb-112">Annak a hálózati biztonsági csoportnak a nevét adja meg, amelynek a parancsmagja nem egy alhálózatról van kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="6b7cb-112">Specifies the name of the network security group that this cmdlet dissociates from a subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b7cb-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b7cb-113">-PassThru</span></span>
<span data-ttu-id="6b7cb-114">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="6b7cb-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="6b7cb-115">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="6b7cb-115">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b7cb-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="6b7cb-116">-Profile</span></span>
<span data-ttu-id="6b7cb-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="6b7cb-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="6b7cb-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="6b7cb-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6b7cb-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="6b7cb-119">-SubnetName</span></span>
<span data-ttu-id="6b7cb-120">Annak az alhálózatnak a neve, amelyből a parancsmag a hálózat biztonsági csoportját szétválasztja.</span><span class="sxs-lookup"><span data-stu-id="6b7cb-120">Specifies the name of a subnet from which this cmdlet dissociates a network security group.</span></span>

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

### <span data-ttu-id="6b7cb-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="6b7cb-121">-VirtualNetworkName</span></span>
<span data-ttu-id="6b7cb-122">A virtuális hálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b7cb-122">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="6b7cb-123">Ez a parancsmag a virtuális hálózatban a hálózat biztonsági csoportját nem társítja a virtuális hálózatból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b7cb-123">This cmdlet disassociates a network security group from a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="6b7cb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b7cb-124">CommonParameters</span></span>
<span data-ttu-id="6b7cb-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b7cb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b7cb-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b7cb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b7cb-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b7cb-127">INPUTS</span></span>

## <span data-ttu-id="6b7cb-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b7cb-128">OUTPUTS</span></span>

## <span data-ttu-id="6b7cb-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b7cb-129">NOTES</span></span>

## <span data-ttu-id="6b7cb-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b7cb-130">RELATED LINKS</span></span>

[<span data-ttu-id="6b7cb-131">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="6b7cb-131">Get-AzureNetworkSecurityGroupForSubnet</span></span>](./Get-AzureNetworkSecurityGroupForSubnet.md)

[<span data-ttu-id="6b7cb-132">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="6b7cb-132">Set-AzureNetworkSecurityGroupToSubnet</span></span>](./Set-AzureNetworkSecurityGroupToSubnet.md)


