---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9E7A170D-512A-4117-85C3-3AA4D6341C6B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97fe847fd183caa7de281b358da579e8df4d5831
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015740"
---
# <span data-ttu-id="874cf-101">Stop-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="874cf-101">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="874cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="874cf-102">SYNOPSIS</span></span>
<span data-ttu-id="874cf-103">Egy futó virtuális hálózati átjáró diagnosztikai munkamenetének leállítása.</span><span class="sxs-lookup"><span data-stu-id="874cf-103">Stops a running virtual network gateway diagnostics session.</span></span>

## <span data-ttu-id="874cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="874cf-104">SYNTAX</span></span>

```
Stop-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="874cf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="874cf-105">DESCRIPTION</span></span>
<span data-ttu-id="874cf-106">A **stop-AzureVirtualNetworkGatewayDiagnostics** parancsmag leállítja a virtuális hálózati átjáró diagnosztikai munkamenetének futását.</span><span class="sxs-lookup"><span data-stu-id="874cf-106">The **Stop-AzureVirtualNetworkGatewayDiagnostics** cmdlet stops a running virtual network gateway diagnostics session.</span></span>
<span data-ttu-id="874cf-107">Ez a parancs a diagnosztikai munkamenet eredményét az Start-AzureVirtualNetworkGatewayDiagnostics parancsmag által megadott tárolási fiókba menti.</span><span class="sxs-lookup"><span data-stu-id="874cf-107">This command saves the results of the diagnostics session to the storage account that the Start-AzureVirtualNetworkGatewayDiagnostics cmdlet specifies.</span></span>

## <span data-ttu-id="874cf-108">Példák</span><span class="sxs-lookup"><span data-stu-id="874cf-108">EXAMPLES</span></span>

## <span data-ttu-id="874cf-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="874cf-109">PARAMETERS</span></span>

### <span data-ttu-id="874cf-110">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="874cf-110">-GatewayId</span></span>
<span data-ttu-id="874cf-111">Az átjáró AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="874cf-111">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="874cf-112">-Profil</span><span class="sxs-lookup"><span data-stu-id="874cf-112">-Profile</span></span>
<span data-ttu-id="874cf-113">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="874cf-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="874cf-114">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="874cf-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="874cf-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="874cf-115">CommonParameters</span></span>
<span data-ttu-id="874cf-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="874cf-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="874cf-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="874cf-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="874cf-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="874cf-118">INPUTS</span></span>

## <span data-ttu-id="874cf-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="874cf-119">OUTPUTS</span></span>

## <span data-ttu-id="874cf-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="874cf-120">NOTES</span></span>

## <span data-ttu-id="874cf-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="874cf-121">RELATED LINKS</span></span>

[<span data-ttu-id="874cf-122">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="874cf-122">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="874cf-123">Start-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="874cf-123">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Start-AzureVirtualNetworkGatewayDiagnostics.md)


