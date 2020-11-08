---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 78DE0AD2-6210-4604-89A8-41915D58BD68
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c40cb0fd38953ff46fa1138dc91f0b9e97ece75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015576"
---
# <span data-ttu-id="70850-101">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="70850-101">Get-AzureSiteRecoveryStorage</span></span>

## <span data-ttu-id="70850-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70850-102">SYNOPSIS</span></span>
<span data-ttu-id="70850-103">Helyreállítási tárterületet kap a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="70850-103">Gets Site Recovery Storages for a vault.</span></span>

## <span data-ttu-id="70850-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70850-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryStorage -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="70850-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="70850-105">DESCRIPTION</span></span>
<span data-ttu-id="70850-106">A **Get-AzureSiteRecoveryStorage** parancsmag Azure-webhely-helyreállítási tárolókat kap az aktuális Azure webhely-helyreállítási boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="70850-106">The **Get-AzureSiteRecoveryStorage** cmdlet gets Azure Site Recovery Storages for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="70850-107">Példák</span><span class="sxs-lookup"><span data-stu-id="70850-107">EXAMPLES</span></span>

### <span data-ttu-id="70850-108">Példa 1: webhely-helyreállítási tárterület beszerzése</span><span class="sxs-lookup"><span data-stu-id="70850-108">Example 1: Get site recovery storage</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryStorage -Server $Servers[0]
Name           : phase2PrimaryStorageClassification
ID             : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
FabricObjectID : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
ServerId       : 774859b0-1966-48cc-9df7-759c441b7a8c
Type           : Classification
FabricType     : VMM

Name           : phase2RecoveryStorageClassification
ID             : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
FabricObjectID : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
ServerId       : 774859b0-1966-48cc-9df7-759c441b7a8c
Type           : Classification
FabricType     : VMM
```

<span data-ttu-id="70850-109">Az első Command parancsmag a **Get-AzureSiteRecoveryServer** parancsmaggal kapja meg az aktuális Azure-webhely helyreállítási boltozatának kiszolgálóit.</span><span class="sxs-lookup"><span data-stu-id="70850-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="70850-110">A parancs a $Servers Array változóban tárolja a webhely-helyreállítási kiszolgálókat.</span><span class="sxs-lookup"><span data-stu-id="70850-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="70850-111">A második parancs beolvassa a webhely-helyreállítási tárterületet az első kiszolgálónak a $Servers tömbben.</span><span class="sxs-lookup"><span data-stu-id="70850-111">The second command gets the site recovery storage for the first server in the $Servers array.</span></span>

## <span data-ttu-id="70850-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70850-112">PARAMETERS</span></span>

### <span data-ttu-id="70850-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="70850-113">-Profile</span></span>
<span data-ttu-id="70850-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="70850-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="70850-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="70850-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="70850-116">-Server</span><span class="sxs-lookup"><span data-stu-id="70850-116">-Server</span></span>
<span data-ttu-id="70850-117">Itt adhatja meg az Azure webhely-helyreállítási tárterület kiszolgálóját.</span><span class="sxs-lookup"><span data-stu-id="70850-117">Specifies a server for Azure Site Recovery Storage.</span></span>
<span data-ttu-id="70850-118">Ha **ASRServer** objektumot szeretne beolvasni, használja a **Get-AzureSiteRecoveryServer** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="70850-118">To obtain an **ASRServer** object, use the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>

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

### <span data-ttu-id="70850-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70850-119">CommonParameters</span></span>
<span data-ttu-id="70850-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70850-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70850-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70850-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70850-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70850-122">INPUTS</span></span>

## <span data-ttu-id="70850-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70850-123">OUTPUTS</span></span>

## <span data-ttu-id="70850-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70850-124">NOTES</span></span>

## <span data-ttu-id="70850-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70850-125">RELATED LINKS</span></span>

[<span data-ttu-id="70850-126">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="70850-126">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)


