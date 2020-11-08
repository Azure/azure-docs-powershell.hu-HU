---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 3EC274C9-9BF6-4B39-BC70-C7F9D780805D
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4081d6d072aadd6a4ae7d09ff57748a8f2cb697
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015580"
---
# <span data-ttu-id="f21c8-101">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="f21c8-101">Get-AzureSiteRecoveryServer</span></span>

## <span data-ttu-id="f21c8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f21c8-102">SYNOPSIS</span></span>
<span data-ttu-id="f21c8-103">A webhely-helyreállítási kiszolgálók regisztrálták a webhely-helyreállítási boltozatot.</span><span class="sxs-lookup"><span data-stu-id="f21c8-103">Gets Site Recovery servers registered a Site Recovery vault.</span></span>

## <span data-ttu-id="f21c8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f21c8-104">SYNTAX</span></span>

### <span data-ttu-id="f21c8-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f21c8-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryServer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f21c8-106">ById</span><span class="sxs-lookup"><span data-stu-id="f21c8-106">ById</span></span>
```
Get-AzureSiteRecoveryServer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f21c8-107">ByName</span><span class="sxs-lookup"><span data-stu-id="f21c8-107">ByName</span></span>
```
Get-AzureSiteRecoveryServer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f21c8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f21c8-108">DESCRIPTION</span></span>
<span data-ttu-id="f21c8-109">A **Get-AzureSiteRecoveryServer** parancsmag a jelenlegi webhely-helyreállítási boltozathoz regisztrált Azure-webhelyek helyreállítási kiszolgálóiról tartalmaz információkat.</span><span class="sxs-lookup"><span data-stu-id="f21c8-109">The **Get-AzureSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="f21c8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f21c8-110">EXAMPLES</span></span>

### <span data-ttu-id="f21c8-111">1. példa: információ kérése egy webhely-helyreállítási kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="f21c8-111">Example 1: Get information about a Site Recovery server</span></span>
```
PS C:\> Get-AzureSiteRecoveryServer
ID              : cd7dec80-1144-4531-9ab3-888b8ab39bee
Name            : server1.contoso.com
LastHeartbeat   : 9/23/2014 3:51:22 PM
ProviderVersion : 3.5.520.0
ServerVersion   : 3.2.7634.0

ID              : f5e713fe-5b6d-4641-9690-6fe74c976b8e
Name            : Server2.contoso.com
LastHeartbeat   : 8/13/2014 2:28:58 PM
ProviderVersion : 3.5
ServerVersion   : 3.2.7510.0
```

<span data-ttu-id="f21c8-112">Ez a parancs információt kap az Azure webhely-helyreállítási kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="f21c8-112">This command gets information about an Azure Site Recovery server.</span></span>

## <span data-ttu-id="f21c8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f21c8-113">PARAMETERS</span></span>

### <span data-ttu-id="f21c8-114">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="f21c8-114">-Id</span></span>
<span data-ttu-id="f21c8-115">A kiszolgáló AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f21c8-115">Specifies the ID of a server.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f21c8-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f21c8-116">-Name</span></span>
<span data-ttu-id="f21c8-117">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f21c8-117">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f21c8-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="f21c8-118">-Profile</span></span>
<span data-ttu-id="f21c8-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="f21c8-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f21c8-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="f21c8-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f21c8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f21c8-121">CommonParameters</span></span>
<span data-ttu-id="f21c8-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f21c8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f21c8-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f21c8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f21c8-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f21c8-124">INPUTS</span></span>

## <span data-ttu-id="f21c8-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f21c8-125">OUTPUTS</span></span>

## <span data-ttu-id="f21c8-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f21c8-126">NOTES</span></span>

## <span data-ttu-id="f21c8-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f21c8-127">RELATED LINKS</span></span>

[<span data-ttu-id="f21c8-128">Azure site Recovery Services-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f21c8-128">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


