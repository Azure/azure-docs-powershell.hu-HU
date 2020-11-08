---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 02396628-5E3E-49A6-8377-3F6DC488FEF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75a083c2f892b7b4f07c37ef978d1babb1dd0cb0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015593"
---
# <span data-ttu-id="aa4ce-101">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="aa4ce-101">Get-AzureSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="aa4ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa4ce-102">SYNOPSIS</span></span>
<span data-ttu-id="aa4ce-103">Védett tárolókat kap a webhelyek helyreállítási boltozatához.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-103">Gets protection containers for a Site Recovery vault.</span></span>

## <span data-ttu-id="aa4ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa4ce-104">SYNTAX</span></span>

### <span data-ttu-id="aa4ce-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aa4ce-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionContainer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="aa4ce-106">ById</span><span class="sxs-lookup"><span data-stu-id="aa4ce-106">ById</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="aa4ce-107">ByName</span><span class="sxs-lookup"><span data-stu-id="aa4ce-107">ByName</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="aa4ce-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa4ce-108">DESCRIPTION</span></span>
<span data-ttu-id="aa4ce-109">A **Get-AzureSiteRecoveryProtectionContainer** parancsmag védett tárolókat kap az aktuális Azure webhely-helyreállítási boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-109">The **Get-AzureSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="aa4ce-110">A védelmi tároló egy logikai tároló a védett objektumokhoz, például a virtuális gépekhez.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-110">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="aa4ce-111">A védelmi házirendek definiálják a védett elemek replikációs beállításait, és a védelemmel ellátott tárolóban használhatók, és egy védett entitásra alkalmazhatók.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-111">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="aa4ce-112">Példák</span><span class="sxs-lookup"><span data-stu-id="aa4ce-112">EXAMPLES</span></span>

### <span data-ttu-id="aa4ce-113">1. példa: védett tárolók beszerzése</span><span class="sxs-lookup"><span data-stu-id="aa4ce-113">Example 1: Get protected containers</span></span>
```
PS C:\> Get-AzureSiteRecoveryProtectionContainer
Name                        : PrimaryCloud
ID                          : fd00d920-79e4-4f2d-a282-a779c0cecb7f_ce995917-c962-45d0-b7f3-9f408a4e1429
FabricObjectId              : fd00d920-79e4-4f2d-a282-a779c0cecb7f
FabricType                  : VMM
Type                        : VMM
ServerId                    : fd00d920-79e4-4f2d-a282-a779c0cecb7f
Role                        : Primary
AvailableProtectionProfiles : {ab01dcbe-9da0-4c31-9564-d6904cfadfde, ad388147-83de-4d2f-a09d-fa46c626747e}
```

<span data-ttu-id="aa4ce-114">Ez a parancs az aktuális boltozat védett tárolóit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-114">This command gets the protected containers for the current vault.</span></span>

## <span data-ttu-id="aa4ce-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa4ce-115">PARAMETERS</span></span>

### <span data-ttu-id="aa4ce-116">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="aa4ce-116">-Id</span></span>
<span data-ttu-id="aa4ce-117">A beolvasott védett tároló AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-117">Specifies the ID of a protected container to get.</span></span>

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

### <span data-ttu-id="aa4ce-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aa4ce-118">-Name</span></span>
<span data-ttu-id="aa4ce-119">A beolvasott védelmi tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-119">Specifies the name of a protection container to get.</span></span>

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

### <span data-ttu-id="aa4ce-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="aa4ce-120">-Profile</span></span>
<span data-ttu-id="aa4ce-121">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aa4ce-122">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aa4ce-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa4ce-123">CommonParameters</span></span>
<span data-ttu-id="aa4ce-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa4ce-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa4ce-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa4ce-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa4ce-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa4ce-126">INPUTS</span></span>

## <span data-ttu-id="aa4ce-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa4ce-127">OUTPUTS</span></span>

## <span data-ttu-id="aa4ce-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa4ce-128">NOTES</span></span>

## <span data-ttu-id="aa4ce-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa4ce-129">RELATED LINKS</span></span>

[<span data-ttu-id="aa4ce-130">Azure site Recovery Services-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="aa4ce-130">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


