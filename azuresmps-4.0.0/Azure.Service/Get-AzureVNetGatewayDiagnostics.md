---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 22E8CB18-8CDD-4992-AB81-E1BB400E6BC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 294e931529b7de939a6a5c20181d48b18da1e892
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016277"
---
# <span data-ttu-id="4c4b5-101">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4c4b5-101">Get-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="4c4b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c4b5-102">SYNOPSIS</span></span>
<span data-ttu-id="4c4b5-103">A diagnosztika jelenlegi állapotát kapja egy virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="4c4b5-103">Gets the current state of diagnostics for a virtual network gateway.</span></span>

## <span data-ttu-id="4c4b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c4b5-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4c4b5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c4b5-105">DESCRIPTION</span></span>
<span data-ttu-id="4c4b5-106">A **Get-AzureVNetGatewayDiagnostics** parancsmag a virtuális hálózati átjárók jelenlegi diagnosztikai állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4c4b5-106">The **Get-AzureVNetGatewayDiagnostics** cmdlet gets the current state of diagnostics for a virtual network gateway.</span></span>
<span data-ttu-id="4c4b5-107">Ha egy olyan bináris nagy objektum (blob) létezik, ahol a **Start-AzureVNetGatewayDiagnostics** mentett egy korábbi diagnosztikai munkamenetet, ez a parancsmag azt is visszaküldi a blob URL-címére, amelyben a parancsmag a diagnosztikai munkamenetet mentette.</span><span class="sxs-lookup"><span data-stu-id="4c4b5-107">If a binary large object (blob) exists where the **Start-AzureVNetGatewayDiagnostics** saved a previous diagnostics session, this cmdlet also returns the URL of the blob where that cmdlet saved that diagnostics session.</span></span>

## <span data-ttu-id="4c4b5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4c4b5-108">EXAMPLES</span></span>

## <span data-ttu-id="4c4b5-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c4b5-109">PARAMETERS</span></span>

### <span data-ttu-id="4c4b5-110">-Profil</span><span class="sxs-lookup"><span data-stu-id="4c4b5-110">-Profile</span></span>
<span data-ttu-id="4c4b5-111">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="4c4b5-111">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="4c4b5-112">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="4c4b5-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4c4b5-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="4c4b5-113">-VNetName</span></span>
<span data-ttu-id="4c4b5-114">A virtuális hálózati átjárót tartalmazó virtuális hálózat, amelynek a parancsmagja a diagnosztikát kapja.</span><span class="sxs-lookup"><span data-stu-id="4c4b5-114">Specifies the virtual network that contains a virtual network gateway for which this cmdlet gets diagnostics.</span></span>

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

### <span data-ttu-id="4c4b5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c4b5-115">CommonParameters</span></span>
<span data-ttu-id="4c4b5-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c4b5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c4b5-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c4b5-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c4b5-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c4b5-118">INPUTS</span></span>

## <span data-ttu-id="4c4b5-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c4b5-119">OUTPUTS</span></span>

## <span data-ttu-id="4c4b5-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c4b5-120">NOTES</span></span>

## <span data-ttu-id="4c4b5-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c4b5-121">RELATED LINKS</span></span>

[<span data-ttu-id="4c4b5-122">Start-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4c4b5-122">Start-AzureVNetGatewayDiagnostics</span></span>](./Start-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="4c4b5-123">Stop-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4c4b5-123">Stop-AzureVNetGatewayDiagnostics</span></span>](./Stop-AzureVNetGatewayDiagnostics.md)


