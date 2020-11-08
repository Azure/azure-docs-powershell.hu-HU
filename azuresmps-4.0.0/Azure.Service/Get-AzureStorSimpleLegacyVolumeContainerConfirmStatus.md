---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 3B4630C1-9885-4BE4-B41E-D98AF5CCD7C3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185072d1bc0d0895d4b6cfaea9470bac107d651a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016553"
---
# <span data-ttu-id="0259a-101">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="0259a-101">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>

## <span data-ttu-id="0259a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0259a-102">SYNOPSIS</span></span>
<span data-ttu-id="0259a-103">A véglegesítési vagy visszagörgetési művelet állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0259a-103">Gets the status of a commit or rollback operation.</span></span>

## <span data-ttu-id="0259a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0259a-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId <String>
 [-LegacyContainerNames <String[]>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0259a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0259a-105">DESCRIPTION</span></span>
<span data-ttu-id="0259a-106">A **Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus** parancsmag a véglegesítési vagy a visszaállítási művelet állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0259a-106">The **Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus** cmdlet gets the status of the commit or rollback operation.</span></span>

## <span data-ttu-id="0259a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0259a-107">EXAMPLES</span></span>

### <span data-ttu-id="0259a-108">Példa 1: befejezett véglegesítési művelet állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="0259a-108">Example 1: Get the status of a completed commit operation</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 2bda2b9b-1361-4787-bc04-1e081218ed76_PS
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 84bf18d8-c459-47a7-b4a8-f82ca8659672_PS
VERBOSE: 2015-04-08 13:51:12 ClientRequestId: e93f9cb7-df58-497e-bb9f-9a6a23e68925_PS


LegacyConfigId             : f16463bd-94a9-4c3c-91c2-7a3ba7120087
CommitComplete             : CloudConfigurationName : OneSDKAzureCloud
                             Operation              : Commit
                             PercentageCompleted    : 100
                             Messages               : 

CommitInProgress           : None
CommitFailed               : None
RollbackComplete           : None
RollbackInProgress         : None
RollbackFailed             : None
CommitOrRollbackNotStarted : None
```

<span data-ttu-id="0259a-109">Ez a parancs a megnevezett tároló véglegesítési műveletének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0259a-109">This command gets the status of a commit operation for the named container.</span></span>
<span data-ttu-id="0259a-110">Ez a művelet Befejezett állapotú.</span><span class="sxs-lookup"><span data-stu-id="0259a-110">This operation has a status of completed.</span></span>

### <span data-ttu-id="0259a-111">2. példa: befejezett visszaállítási művelet állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="0259a-111">Example 2: Get the status of a completed rollback operation</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 2bda2b9b-1361-4787-bc04-1e081218ed76_PS
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 84bf18d8-c459-47a7-b4a8-f82ca8659672_PS
VERBOSE: 2015-04-08 13:51:12 ClientRequestId: e93f9cb7-df58-497e-bb9f-9a6a23e68925_PS


LegacyConfigId             : f16463bd-94a9-4c3c-91c2-7a3ba7120087
CommitComplete             : None
CommitInProgress           : None
CommitFailed               : None
RollbackComplete           : CloudConfigurationName : OneSDKAzureCloud
                             Operation              : Rollback
                             PercentageCompleted    : 100
                             Messages               : 

RollbackInProgress         : None
RollbackFailed             : None
CommitOrRollbackNotStarted : None
```

<span data-ttu-id="0259a-112">Ez a parancs a megnevezett tároló visszagörgetési műveletének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0259a-112">This command gets the status of a rollback operation for the named container.</span></span>
<span data-ttu-id="0259a-113">Ez a művelet Befejezett állapotú.</span><span class="sxs-lookup"><span data-stu-id="0259a-113">This operation has a status of completed.</span></span>

## <span data-ttu-id="0259a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0259a-114">PARAMETERS</span></span>

### <span data-ttu-id="0259a-115">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="0259a-115">-LegacyConfigId</span></span>
<span data-ttu-id="0259a-116">A régi készülék konfigurációjának egyedi AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0259a-116">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="0259a-117">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="0259a-117">-LegacyContainerNames</span></span>
<span data-ttu-id="0259a-118">Az áttelepítési terv által érintett mennyiségi tárolók neveinek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0259a-118">Specifies an array of volume container names for which the migration plan applies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0259a-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="0259a-119">-Profile</span></span>
<span data-ttu-id="0259a-120">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="0259a-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="0259a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0259a-121">CommonParameters</span></span>
<span data-ttu-id="0259a-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0259a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0259a-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0259a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0259a-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0259a-124">INPUTS</span></span>

### <span data-ttu-id="0259a-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="0259a-125">None</span></span>

## <span data-ttu-id="0259a-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0259a-126">OUTPUTS</span></span>

### <span data-ttu-id="0259a-127">ConfirmMigrationStatusMsg</span><span class="sxs-lookup"><span data-stu-id="0259a-127">ConfirmMigrationStatusMsg</span></span>
<span data-ttu-id="0259a-128">Ez a parancsmag visszaadja az áttelepítési művelet megerősítésének állapotát.</span><span class="sxs-lookup"><span data-stu-id="0259a-128">This cmdlet returns the status of the confirm migration operation that is performed.</span></span>

## <span data-ttu-id="0259a-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0259a-129">NOTES</span></span>

## <span data-ttu-id="0259a-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0259a-130">RELATED LINKS</span></span>

[<span data-ttu-id="0259a-131">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="0259a-131">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Confirm-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="0259a-132">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="0259a-132">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)


