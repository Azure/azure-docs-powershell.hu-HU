---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8AD101BA-9275-4B2B-BB31-99FC34B8D1E8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1ac1d91bc084c9e1b17debf154b2a44c144ce312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016275"
---
# <span data-ttu-id="29640-101">Get-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="29640-101">Get-AzureVNetGatewayKey</span></span>

## <span data-ttu-id="29640-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29640-102">SYNOPSIS</span></span>
<span data-ttu-id="29640-103">A virtuális hálózati átjáró és a helyi hálózat webhelye közötti kapcsolat előmegosztott kulcsát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="29640-103">Gets the pre-shared key for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="29640-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29640-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="29640-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="29640-105">DESCRIPTION</span></span>
<span data-ttu-id="29640-106">A **Get-AzureVNetGatewayKey** parancsmag a virtuális hálózati átjáró és a helyi hálózati webhely közötti kapcsolat előmegosztott kulcsát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="29640-106">The **Get-AzureVNetGatewayKey** cmdlet gets the pre-shared key for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="29640-107">Példák</span><span class="sxs-lookup"><span data-stu-id="29640-107">EXAMPLES</span></span>

## <span data-ttu-id="29640-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29640-108">PARAMETERS</span></span>

### <span data-ttu-id="29640-109">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="29640-109">-LocalNetworkSiteName</span></span>
<span data-ttu-id="29640-110">Annak a helyi hálózati webhelynek a neve, amely a virtuális hálózati átjáróhoz csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="29640-110">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="29640-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="29640-111">-Profile</span></span>
<span data-ttu-id="29640-112">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="29640-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="29640-113">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="29640-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="29640-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="29640-114">-VNetName</span></span>
<span data-ttu-id="29640-115">Annak a virtuális hálózatnak a megadása, amelyhez ez a parancsmag a kapcsolatok megosztott kulcsát kapja.</span><span class="sxs-lookup"><span data-stu-id="29640-115">Specifies the virtual network for which this cmdlet gets the shared key for connections.</span></span>

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

### <span data-ttu-id="29640-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29640-116">CommonParameters</span></span>
<span data-ttu-id="29640-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29640-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29640-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29640-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29640-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29640-119">INPUTS</span></span>

## <span data-ttu-id="29640-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29640-120">OUTPUTS</span></span>

## <span data-ttu-id="29640-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29640-121">NOTES</span></span>

## <span data-ttu-id="29640-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29640-122">RELATED LINKS</span></span>

[<span data-ttu-id="29640-123">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="29640-123">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


