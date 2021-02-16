---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 615D2C5D-AB31-45DB-9535-9B9C8E957322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a5701fc6308f1884bbf0237887a223a62a58669
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411585"
---
# <span data-ttu-id="5b8ec-101">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="5b8ec-101">Get-AzureSiteRecoveryNetwork</span></span>

## <span data-ttu-id="5b8ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b8ec-102">SYNOPSIS</span></span>
<span data-ttu-id="5b8ec-103">Információkat kap a webhely-helyreállítás által kezelt hálózatokról az aktuális tárolóban.</span><span class="sxs-lookup"><span data-stu-id="5b8ec-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="5b8ec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5b8ec-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryNetwork -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5b8ec-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5b8ec-105">DESCRIPTION</span></span>
<span data-ttu-id="5b8ec-106">A **Get-AzureSiteRecoveryNetwork** parancsmag információkat kap az aktuális webhely-helyreállítási tároló Azure Webhely-helyreállítási hálózatairól.</span><span class="sxs-lookup"><span data-stu-id="5b8ec-106">The **Get-AzureSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Site Recovery vault.</span></span>

## <span data-ttu-id="5b8ec-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5b8ec-107">EXAMPLES</span></span>

### <span data-ttu-id="5b8ec-108">1. példa: Webhely-helyreállítási hálózatok leszerzése</span><span class="sxs-lookup"><span data-stu-id="5b8ec-108">Example 1: Get site recovery networks</span></span>
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

<span data-ttu-id="5b8ec-109">Az első parancsmag a **Get-AzureSiteRecoveryServer** parancsmag használatával szerezze be az aktuális Azure Site Recovery tároló kiszolgálóit.</span><span class="sxs-lookup"><span data-stu-id="5b8ec-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="5b8ec-110">A parancs a webhely-helyreállítási kiszolgálókat a $Servers tárolja.</span><span class="sxs-lookup"><span data-stu-id="5b8ec-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="5b8ec-111">A második parancs a tömb első kiszolgálójának webhely-helyreállítási hálózatát $Servers le.</span><span class="sxs-lookup"><span data-stu-id="5b8ec-111">The second command gets the site recovery network for the first server in the $Servers array.</span></span>

## <span data-ttu-id="5b8ec-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b8ec-112">PARAMETERS</span></span>

### <span data-ttu-id="5b8ec-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="5b8ec-113">-Profile</span></span>
<span data-ttu-id="5b8ec-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvas.</span><span class="sxs-lookup"><span data-stu-id="5b8ec-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5b8ec-115">Ha nem ad meg profilt, ez a parancsmag a helyi alapértelmezett profilból olvassa be.</span><span class="sxs-lookup"><span data-stu-id="5b8ec-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5b8ec-116">-Server</span><span class="sxs-lookup"><span data-stu-id="5b8ec-116">-Server</span></span>
<span data-ttu-id="5b8ec-117">Egy webhely-helyreállítási kiszolgálót ad meg.</span><span class="sxs-lookup"><span data-stu-id="5b8ec-117">Specifies a Site Recovery server.</span></span>

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

### <span data-ttu-id="5b8ec-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b8ec-118">CommonParameters</span></span>
<span data-ttu-id="5b8ec-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b8ec-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b8ec-120">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b8ec-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b8ec-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b8ec-121">INPUTS</span></span>

## <span data-ttu-id="5b8ec-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b8ec-122">OUTPUTS</span></span>

## <span data-ttu-id="5b8ec-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5b8ec-123">NOTES</span></span>

## <span data-ttu-id="5b8ec-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b8ec-124">RELATED LINKS</span></span>




