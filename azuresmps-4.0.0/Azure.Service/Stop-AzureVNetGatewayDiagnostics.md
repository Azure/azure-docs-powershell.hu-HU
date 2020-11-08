---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 706CBF65-C796-4525-BAEB-AAFAD44C0464
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37c2ce3b32d23f7c5bb682d2116de84cc90f047
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016019"
---
# <span data-ttu-id="4314d-101">Stop-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4314d-101">Stop-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="4314d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4314d-102">SYNOPSIS</span></span>
<span data-ttu-id="4314d-103">Egy futó VPN-átjáró diagnosztikai munkamenetének leállítása.</span><span class="sxs-lookup"><span data-stu-id="4314d-103">Stops a running VPN gateway diagnostics session.</span></span>

## <span data-ttu-id="4314d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4314d-104">SYNTAX</span></span>

```
Stop-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4314d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4314d-105">DESCRIPTION</span></span>
<span data-ttu-id="4314d-106">A **stop-AzureVNetGatewayDiagnostics** parancsmag leállítja a virtuális MAGÁNHÁLÓZATI (VPN-) átjáró diagnosztikai munkamenetét.</span><span class="sxs-lookup"><span data-stu-id="4314d-106">The **Stop-AzureVNetGatewayDiagnostics** cmdlet stops a running virtual private network (VPN) gateway diagnostics session.</span></span>
<span data-ttu-id="4314d-107">Ez a parancs a diagnosztikai munkamenet eredményét a **Start-AzureVNetGatewayDiagnostics** parancsmag által megadott tárolási fiókba menti.</span><span class="sxs-lookup"><span data-stu-id="4314d-107">This command saves the results of the diagnostics session to the storage account that the **Start-AzureVNetGatewayDiagnostics** cmdlet specifies.</span></span>

## <span data-ttu-id="4314d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4314d-108">EXAMPLES</span></span>

## <span data-ttu-id="4314d-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4314d-109">PARAMETERS</span></span>

### <span data-ttu-id="4314d-110">-Profil</span><span class="sxs-lookup"><span data-stu-id="4314d-110">-Profile</span></span>
<span data-ttu-id="4314d-111">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="4314d-111">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="4314d-112">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="4314d-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4314d-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="4314d-113">-VNetName</span></span>
<span data-ttu-id="4314d-114">Azt a virtuális hálózati átjárót tartalmazó virtuális hálózat, amelyhez ez a parancsmag leállítja a diagnosztikát.</span><span class="sxs-lookup"><span data-stu-id="4314d-114">Specifies the virtual network that contains a virtual network gateway for which this cmdlet stops diagnostics.</span></span>

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

### <span data-ttu-id="4314d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4314d-115">CommonParameters</span></span>
<span data-ttu-id="4314d-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4314d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4314d-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4314d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4314d-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4314d-118">INPUTS</span></span>

## <span data-ttu-id="4314d-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4314d-119">OUTPUTS</span></span>

## <span data-ttu-id="4314d-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4314d-120">NOTES</span></span>

## <span data-ttu-id="4314d-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4314d-121">RELATED LINKS</span></span>

[<span data-ttu-id="4314d-122">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4314d-122">Get-AzureVNetGatewayDiagnostics</span></span>](./Get-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="4314d-123">Start-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4314d-123">Start-AzureVNetGatewayDiagnostics</span></span>](./Start-AzureVNetGatewayDiagnostics.md)


