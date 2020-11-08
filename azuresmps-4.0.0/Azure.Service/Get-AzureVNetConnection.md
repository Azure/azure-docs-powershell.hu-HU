---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7B749B29-9820-4E23-B5AF-F5535251629A
online version: ''
schema: 2.0.0
ms.openlocfilehash: ec94df29fb23dd7c82d79304c2e48aab225ed224
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016287"
---
# <span data-ttu-id="14ffc-101">Get-AzureVNetConnection</span><span class="sxs-lookup"><span data-stu-id="14ffc-101">Get-AzureVNetConnection</span></span>

## <span data-ttu-id="14ffc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="14ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="14ffc-103">Az Azure virtuális hálózattal való kapcsolódást kapja.</span><span class="sxs-lookup"><span data-stu-id="14ffc-103">Gets connections to an Azure virtual network.</span></span>

## <span data-ttu-id="14ffc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="14ffc-104">SYNTAX</span></span>

```
Get-AzureVNetConnection -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="14ffc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="14ffc-105">DESCRIPTION</span></span>
<span data-ttu-id="14ffc-106">A **Get-AzureVNetConnection** parancsmag egy olyan objektumot ad eredményül, amely az Azure virtuális hálózat minden aktív virtuális MAGÁNHÁLÓZATI (VPN-) kapcsolatát megadja.</span><span class="sxs-lookup"><span data-stu-id="14ffc-106">The **Get-AzureVNetConnection** cmdlet returns an object that specifies all active virtual private network (VPN) connections to an Azure virtual network.</span></span>
<span data-ttu-id="14ffc-107">A VPN-kapcsolatok közé tartozik a helyközi, webhelyek közötti virtuális magánhálózatok és virtuális hálózat a virtuális hálózati kapcsolatokhoz.</span><span class="sxs-lookup"><span data-stu-id="14ffc-107">VPN connections include cross premises site-to-site VPNs and virtual network to virtual network connections.</span></span>

## <span data-ttu-id="14ffc-108">Példák</span><span class="sxs-lookup"><span data-stu-id="14ffc-108">EXAMPLES</span></span>

## <span data-ttu-id="14ffc-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="14ffc-109">PARAMETERS</span></span>

### <span data-ttu-id="14ffc-110">-Profil</span><span class="sxs-lookup"><span data-stu-id="14ffc-110">-Profile</span></span>
<span data-ttu-id="14ffc-111">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="14ffc-111">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="14ffc-112">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="14ffc-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="14ffc-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="14ffc-113">-VNetName</span></span>
<span data-ttu-id="14ffc-114">Annak a virtuális hálózatnak a neve, amelyből a parancsmag a kapcsolatokat visszaadja.</span><span class="sxs-lookup"><span data-stu-id="14ffc-114">Specifies the name of the virtual network from which this cmdlet returns connections.</span></span>

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

### <span data-ttu-id="14ffc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14ffc-115">CommonParameters</span></span>
<span data-ttu-id="14ffc-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="14ffc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14ffc-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14ffc-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14ffc-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="14ffc-118">INPUTS</span></span>

## <span data-ttu-id="14ffc-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14ffc-119">OUTPUTS</span></span>

## <span data-ttu-id="14ffc-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="14ffc-120">NOTES</span></span>

## <span data-ttu-id="14ffc-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14ffc-121">RELATED LINKS</span></span>

