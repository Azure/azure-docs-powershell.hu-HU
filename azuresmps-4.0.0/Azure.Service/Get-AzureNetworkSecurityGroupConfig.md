---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: FCB3C8EB-EAA6-48E3-A1A5-DB3050821BD8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 402aa39fb1476d6b3bc69902148e71549fccb3fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016333"
---
# <span data-ttu-id="2a7e3-101">Get-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="2a7e3-101">Get-AzureNetworkSecurityGroupConfig</span></span>

## <span data-ttu-id="2a7e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2a7e3-102">SYNOPSIS</span></span>
<span data-ttu-id="2a7e3-103">Megkeresi a hálózat biztonsági csoportjának részleteit.</span><span class="sxs-lookup"><span data-stu-id="2a7e3-103">Gets details for a network security group.</span></span>

## <span data-ttu-id="2a7e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2a7e3-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroupConfig [-Detailed] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a7e3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2a7e3-105">DESCRIPTION</span></span>
<span data-ttu-id="2a7e3-106">A **Get-AzureNetworkSecurityGroupConfig** parancsmag egy hálózati biztonsági csoport részleteit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="2a7e3-106">The **Get-AzureNetworkSecurityGroupConfig** cmdlet returns details for a network security group.</span></span>
<span data-ttu-id="2a7e3-107">A hálózati biztonsági szabályok megjelenítéséhez adja meg a *részletes* paramétert.</span><span class="sxs-lookup"><span data-stu-id="2a7e3-107">Specify the *Detailed* parameter to display the network security rules.</span></span>

## <span data-ttu-id="2a7e3-108">Példák</span><span class="sxs-lookup"><span data-stu-id="2a7e3-108">EXAMPLES</span></span>

## <span data-ttu-id="2a7e3-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2a7e3-109">PARAMETERS</span></span>

### <span data-ttu-id="2a7e3-110">– Részletes</span><span class="sxs-lookup"><span data-stu-id="2a7e3-110">-Detailed</span></span>
<span data-ttu-id="2a7e3-111">Jelzi, hogy ez a parancsmag a hálózat biztonsági szabályait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="2a7e3-111">Indicates that this cmdlet displays the network security rules.</span></span>

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

### <span data-ttu-id="2a7e3-112">-Profil</span><span class="sxs-lookup"><span data-stu-id="2a7e3-112">-Profile</span></span>
<span data-ttu-id="2a7e3-113">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="2a7e3-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2a7e3-114">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="2a7e3-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2a7e3-115">-VM</span><span class="sxs-lookup"><span data-stu-id="2a7e3-115">-VM</span></span>
<span data-ttu-id="2a7e3-116">Azt a virtuális gépet adja meg, amelynek a parancsmagja a hálózati biztonsági csoport adatait kapja.</span><span class="sxs-lookup"><span data-stu-id="2a7e3-116">Specifies the virtual machine for which this cmdlet gets the details of a network security group.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a7e3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a7e3-117">CommonParameters</span></span>
<span data-ttu-id="2a7e3-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2a7e3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a7e3-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a7e3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a7e3-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a7e3-120">INPUTS</span></span>

## <span data-ttu-id="2a7e3-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a7e3-121">OUTPUTS</span></span>

## <span data-ttu-id="2a7e3-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2a7e3-122">NOTES</span></span>

## <span data-ttu-id="2a7e3-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a7e3-123">RELATED LINKS</span></span>

[<span data-ttu-id="2a7e3-124">Új – AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2a7e3-124">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="2a7e3-125">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2a7e3-125">Remove-AzureNetworkSecurityGroup</span></span>](./Remove-AzureNetworkSecurityGroup.md)


