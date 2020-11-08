---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A14F9105-1422-4073-96CF-E75CFC039E05
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7eaf1af2efe3f93f4e0a44d54e1f07ea52166942
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015829"
---
# <span data-ttu-id="9da3b-101">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="9da3b-101">Set-AzureNetworkSecurityGroupToSubnet</span></span>

## <span data-ttu-id="9da3b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9da3b-102">SYNOPSIS</span></span>
<span data-ttu-id="9da3b-103">Hálózati biztonsági csoport társítása egy alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="9da3b-103">Associates a network security group to a subnet.</span></span>

## <span data-ttu-id="9da3b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9da3b-104">SYNTAX</span></span>

```
Set-AzureNetworkSecurityGroupToSubnet -Name <String> -VirtualNetworkName <String> -SubnetName <String> [-Force]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9da3b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9da3b-105">DESCRIPTION</span></span>
<span data-ttu-id="9da3b-106">A **set-AzureNetworkSecurityGroupToSubnet** parancsmag az Azure Network biztonsági csoportját társítja egy alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="9da3b-106">The **Set-AzureNetworkSecurityGroupToSubnet** cmdlet associates an Azure network security group to a subnet.</span></span>

## <span data-ttu-id="9da3b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9da3b-107">EXAMPLES</span></span>

## <span data-ttu-id="9da3b-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9da3b-108">PARAMETERS</span></span>

### <span data-ttu-id="9da3b-109">-Force</span><span class="sxs-lookup"><span data-stu-id="9da3b-109">-Force</span></span>
<span data-ttu-id="9da3b-110">Azt jelzi, hogy ez a parancsmag nem kéri, hogy erősítse meg egy korábbi hálózati biztonsági csoport eltávolítását az alhálózatról.</span><span class="sxs-lookup"><span data-stu-id="9da3b-110">Indicates that this cmdlet does not prompt you to confirm the removal of a previous network security group from the subnet.</span></span>

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

### <span data-ttu-id="9da3b-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9da3b-111">-Name</span></span>
<span data-ttu-id="9da3b-112">Annak a hálózati biztonsági csoportnak a neve, amelyhez a parancsmag társít egy alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="9da3b-112">Specifies the name of the network security group that this cmdlet associates to a subnet.</span></span>

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

### <span data-ttu-id="9da3b-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9da3b-113">-PassThru</span></span>
<span data-ttu-id="9da3b-114">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="9da3b-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="9da3b-115">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9da3b-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9da3b-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="9da3b-116">-Profile</span></span>
<span data-ttu-id="9da3b-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="9da3b-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9da3b-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="9da3b-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9da3b-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="9da3b-119">-SubnetName</span></span>
<span data-ttu-id="9da3b-120">Annak az alhálózatnak a neve, amelyhez ez a parancsmag egy hálózati biztonsági csoportot társít.</span><span class="sxs-lookup"><span data-stu-id="9da3b-120">Specifies the name of a subnet to which this cmdlet associates a network security group.</span></span>

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

### <span data-ttu-id="9da3b-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="9da3b-121">-VirtualNetworkName</span></span>
<span data-ttu-id="9da3b-122">A virtuális hálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9da3b-122">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="9da3b-123">Ez a parancsmag egy hálózati biztonsági csoportot társít a virtuális hálózat azon alhálózatához, amelyhez ez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="9da3b-123">This cmdlet associates a network security group to a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="9da3b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9da3b-124">CommonParameters</span></span>
<span data-ttu-id="9da3b-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9da3b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9da3b-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9da3b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9da3b-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9da3b-127">INPUTS</span></span>

## <span data-ttu-id="9da3b-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9da3b-128">OUTPUTS</span></span>

## <span data-ttu-id="9da3b-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9da3b-129">NOTES</span></span>

## <span data-ttu-id="9da3b-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9da3b-130">RELATED LINKS</span></span>

[<span data-ttu-id="9da3b-131">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="9da3b-131">Get-AzureNetworkSecurityGroupForSubnet</span></span>](./Get-AzureNetworkSecurityGroupForSubnet.md)

[<span data-ttu-id="9da3b-132">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="9da3b-132">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>](./Remove-AzureNetworkSecurityGroupFromSubnet.md)


