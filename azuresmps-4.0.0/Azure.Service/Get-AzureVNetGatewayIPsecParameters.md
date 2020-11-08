---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B7E2561D-0FE8-4B34-9188-E89AA0B5C9DD
online version: ''
schema: 2.0.0
ms.openlocfilehash: dce79fc891018c3100140581e89639dbc76b543d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016276"
---
# <span data-ttu-id="69102-101">Get-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="69102-101">Get-AzureVNetGatewayIPsecParameters</span></span>

## <span data-ttu-id="69102-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69102-102">SYNOPSIS</span></span>
<span data-ttu-id="69102-103">A virtuális hálózati átjáró és a helyi hálózati webhely közötti kapcsolat IPsec-paramétereit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="69102-103">Gets IPsec parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="69102-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69102-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayIPsecParameters -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="69102-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="69102-105">DESCRIPTION</span></span>
<span data-ttu-id="69102-106">A **Get-AzureVNetGatewayIPsecParameters** parancsmag az Internet Protocol Security (IPSec) és az internetes KULCSCSERE (IKE) paramétereit kapja meg a virtuális hálózati átjáró és egy helyi hálózati webhely közötti kapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="69102-106">The **Get-AzureVNetGatewayIPsecParameters** cmdlet gets current Internet Protocol security (IPsec) and Internet Key Exchange (IKE) parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="69102-107">Példák</span><span class="sxs-lookup"><span data-stu-id="69102-107">EXAMPLES</span></span>

## <span data-ttu-id="69102-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69102-108">PARAMETERS</span></span>

### <span data-ttu-id="69102-109">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="69102-109">-LocalNetworkSiteName</span></span>
<span data-ttu-id="69102-110">Annak a helyi hálózati webhelynek a neve, amely a virtuális hálózati átjáróhoz csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="69102-110">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="69102-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="69102-111">-Profile</span></span>
<span data-ttu-id="69102-112">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="69102-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="69102-113">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="69102-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="69102-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="69102-114">-VNetName</span></span>
<span data-ttu-id="69102-115">Annak a virtuális hálózatnak a megadása, amelyhez ez a parancsmag az IPsec-paramétereket kapja a kapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="69102-115">Specifies the virtual network for which this cmdlet gets IPsec parameters for the connection.</span></span>

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

### <span data-ttu-id="69102-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69102-116">CommonParameters</span></span>
<span data-ttu-id="69102-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69102-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69102-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69102-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69102-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69102-119">INPUTS</span></span>

## <span data-ttu-id="69102-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69102-120">OUTPUTS</span></span>

## <span data-ttu-id="69102-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69102-121">NOTES</span></span>

## <span data-ttu-id="69102-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69102-122">RELATED LINKS</span></span>

[<span data-ttu-id="69102-123">Set-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="69102-123">Set-AzureVNetGatewayIPsecParameters</span></span>](./Set-AzureVNetGatewayIPsecParameters.md)


