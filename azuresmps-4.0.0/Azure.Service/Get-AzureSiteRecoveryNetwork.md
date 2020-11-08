---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 615D2C5D-AB31-45DB-9535-9B9C8E957322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 96b51b49d76093be96eeab26417f4a70f70c4627
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015592"
---
# <span data-ttu-id="69998-101">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="69998-101">Get-AzureSiteRecoveryNetwork</span></span>

## <span data-ttu-id="69998-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69998-102">SYNOPSIS</span></span>
<span data-ttu-id="69998-103">Információt kap a webhelyek helyreállítása által kezelt hálózatokról az aktuális boltozatra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="69998-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="69998-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69998-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryNetwork -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="69998-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="69998-105">DESCRIPTION</span></span>
<span data-ttu-id="69998-106">A **Get-AzureSiteRecoveryNetwork** parancsmag információkat kap az Azure webhely-helyreállítási hálózatokról az aktuális webhely-helyreállítási boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="69998-106">The **Get-AzureSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Site Recovery vault.</span></span>

## <span data-ttu-id="69998-107">Példák</span><span class="sxs-lookup"><span data-stu-id="69998-107">EXAMPLES</span></span>

### <span data-ttu-id="69998-108">Példa 1: webhely-helyreállítási hálózatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="69998-108">Example 1: Get site recovery networks</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetwork -Server $Servers[0]
Name                : phase2RecoveryVMNetwork
ID                  : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
FabricObjectID      : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}

Name                : phase2PrimaryVMNetwork
ID                  : d903e2c6-3141-4cef-bfe1-04616cd43cbb
FabricObjectID      : d903e2c6-3141-4cef-bfe1-04616cd43cbb
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}
```

<span data-ttu-id="69998-109">Az első Command parancsmag a **Get-AzureSiteRecoveryServer** parancsmaggal kapja meg az aktuális Azure-webhely helyreállítási boltozatának kiszolgálóit.</span><span class="sxs-lookup"><span data-stu-id="69998-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="69998-110">A parancs a $Servers Array változóban tárolja a webhely-helyreállítási kiszolgálókat.</span><span class="sxs-lookup"><span data-stu-id="69998-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="69998-111">A második parancs a hely helyreállítási hálózatát kapja meg az első kiszolgálónak a $Servers tömbben.</span><span class="sxs-lookup"><span data-stu-id="69998-111">The second command gets the site recovery network for the first server in the $Servers array.</span></span>

## <span data-ttu-id="69998-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69998-112">PARAMETERS</span></span>

### <span data-ttu-id="69998-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="69998-113">-Profile</span></span>
<span data-ttu-id="69998-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="69998-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="69998-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="69998-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="69998-116">-Server</span><span class="sxs-lookup"><span data-stu-id="69998-116">-Server</span></span>
<span data-ttu-id="69998-117">Webhely-helyreállítási kiszolgálót ad meg.</span><span class="sxs-lookup"><span data-stu-id="69998-117">Specifies a Site Recovery server.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69998-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69998-118">CommonParameters</span></span>
<span data-ttu-id="69998-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69998-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69998-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69998-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69998-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69998-121">INPUTS</span></span>

## <span data-ttu-id="69998-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69998-122">OUTPUTS</span></span>

## <span data-ttu-id="69998-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69998-123">NOTES</span></span>

## <span data-ttu-id="69998-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69998-124">RELATED LINKS</span></span>

[<span data-ttu-id="69998-125">Azure site Recovery Services-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="69998-125">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


