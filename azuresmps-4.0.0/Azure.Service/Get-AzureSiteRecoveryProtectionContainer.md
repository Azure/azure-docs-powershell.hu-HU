---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 02396628-5E3E-49A6-8377-3F6DC488FEF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee948161f101b83a4892441286b760a044e64358
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405822"
---
# <span data-ttu-id="ee899-101">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ee899-101">Get-AzureSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="ee899-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee899-102">SYNOPSIS</span></span>
<span data-ttu-id="ee899-103">Védelmi tárolókat kap egy webhely-helyreállítási tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="ee899-103">Gets protection containers for a Site Recovery vault.</span></span>

## <span data-ttu-id="ee899-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ee899-104">SYNTAX</span></span>

### <span data-ttu-id="ee899-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ee899-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionContainer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ee899-106">ById</span><span class="sxs-lookup"><span data-stu-id="ee899-106">ById</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ee899-107">ByName</span><span class="sxs-lookup"><span data-stu-id="ee899-107">ByName</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ee899-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ee899-108">DESCRIPTION</span></span>
<span data-ttu-id="ee899-109">A **Get-AzureSiteRecoveryProtectionContainer** parancsmag védelmi tárolókat kap az aktuális Azure Site Recovery tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="ee899-109">The **Get-AzureSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="ee899-110">A védelmi tároló a védett objektumok, például a virtuális gépek logikai tárolója.</span><span class="sxs-lookup"><span data-stu-id="ee899-110">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="ee899-111">A védelmi házirendek replikációs beállításokat definiálnak a védett elemekhez, és egy védelmi tárolóhoz társítva egy védett entitásra alkalmazhatók.</span><span class="sxs-lookup"><span data-stu-id="ee899-111">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="ee899-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ee899-112">EXAMPLES</span></span>

### <span data-ttu-id="ee899-113">1. példa: Védett tárolók lekérte</span><span class="sxs-lookup"><span data-stu-id="ee899-113">Example 1: Get protected containers</span></span>
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

<span data-ttu-id="ee899-114">Ez a parancs az aktuális tároló védett tárolóit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ee899-114">This command gets the protected containers for the current vault.</span></span>

## <span data-ttu-id="ee899-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee899-115">PARAMETERS</span></span>

### <span data-ttu-id="ee899-116">-Id</span><span class="sxs-lookup"><span data-stu-id="ee899-116">-Id</span></span>
<span data-ttu-id="ee899-117">Egy lekért védett tároló azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee899-117">Specifies the ID of a protected container to get.</span></span>

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

### <span data-ttu-id="ee899-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ee899-118">-Name</span></span>
<span data-ttu-id="ee899-119">Megadja a behozni megfelelő védelmi tároló nevét.</span><span class="sxs-lookup"><span data-stu-id="ee899-119">Specifies the name of a protection container to get.</span></span>

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

### <span data-ttu-id="ee899-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="ee899-120">-Profile</span></span>
<span data-ttu-id="ee899-121">Azt az Azure-profilt adja meg, amelyből a parancsmag olvas.</span><span class="sxs-lookup"><span data-stu-id="ee899-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ee899-122">Ha nem ad meg profilt, ez a parancsmag a helyi alapértelmezett profilból olvassa be.</span><span class="sxs-lookup"><span data-stu-id="ee899-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ee899-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee899-123">CommonParameters</span></span>
<span data-ttu-id="ee899-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee899-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee899-125">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee899-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee899-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee899-126">INPUTS</span></span>

## <span data-ttu-id="ee899-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee899-127">OUTPUTS</span></span>

## <span data-ttu-id="ee899-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ee899-128">NOTES</span></span>

## <span data-ttu-id="ee899-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee899-129">RELATED LINKS</span></span>




