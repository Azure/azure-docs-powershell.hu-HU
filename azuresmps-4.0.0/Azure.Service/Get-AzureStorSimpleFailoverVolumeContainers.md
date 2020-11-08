---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BABBA19E-5833-452C-9E36-811EAE7C20F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb326281058f0ff9280c4b87c0530241ece801e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015561"
---
# <span data-ttu-id="e14b0-101">Get-AzureStorSimpleFailoverVolumeContainers</span><span class="sxs-lookup"><span data-stu-id="e14b0-101">Get-AzureStorSimpleFailoverVolumeContainers</span></span>

## <span data-ttu-id="e14b0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e14b0-102">SYNOPSIS</span></span>
<span data-ttu-id="e14b0-103">A kötet tároló csoportjának beolvasása az eszközök feladatátvételéhez.</span><span class="sxs-lookup"><span data-stu-id="e14b0-103">Gets the volume container groups for device failover.</span></span>

## <span data-ttu-id="e14b0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e14b0-104">SYNTAX</span></span>

### <span data-ttu-id="e14b0-105">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="e14b0-105">IdentifyById</span></span>
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e14b0-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="e14b0-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e14b0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e14b0-107">DESCRIPTION</span></span>
<span data-ttu-id="e14b0-108">A **Get-AzureStorSimpleFailoverVolumeContainers** parancsmag a kötet-tároló csoportokat kapja meg az eszközök feladatátvételéhez.</span><span class="sxs-lookup"><span data-stu-id="e14b0-108">The **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet gets the volume container groups for device failover.</span></span>
<span data-ttu-id="e14b0-109">Adjon át egyetlen **VolumeContainer** -csoportot vagy **VolumeContainer** -csoportot a **Start-AzureStorSimpleDeviceFailover** parancsmagba.</span><span class="sxs-lookup"><span data-stu-id="e14b0-109">Pass a single **VolumeContainer** group or an array of **VolumeContainer** groups to the **Start-AzureStorSimpleDeviceFailover** cmdlet.</span></span>
<span data-ttu-id="e14b0-110">Csak azok a csoportok jogosultak a feladatátvételre, amelyek $True értékkel rendelkeznek a **IsDCGroupEligibleForDR** tulajdonságban.</span><span class="sxs-lookup"><span data-stu-id="e14b0-110">Only groups that have a value of $True for the **IsDCGroupEligibleForDR** property are eligible for failover.</span></span>

## <span data-ttu-id="e14b0-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e14b0-111">EXAMPLES</span></span>

### <span data-ttu-id="e14b0-112">1. példa: feladatátvevő mennyiségi tárolók beszerzése</span><span class="sxs-lookup"><span data-stu-id="e14b0-112">Example 1: Get failover volume containers</span></span>
```
PS C:\>Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7"

DCGroup                    IneligibilityMessage          IsDCGroupEligibleForDR
-------                    --------------------          ----------------------
{VolumeContainer1889078...                                                 True
{VC_01}                    No cloud snapshot found                        False
{VolumeContainer7306959}   No cloud snapshot found                        False
{VolumeContainer407850151} No cloud snapshot found                        False
```

<span data-ttu-id="e14b0-113">Ez a parancs feladatátvevő mennyiségi tárolókat kap.</span><span class="sxs-lookup"><span data-stu-id="e14b0-113">This command gets failover volume containers.</span></span>
<span data-ttu-id="e14b0-114">Csak azok az DCGroups használhatók, amelyekben az **IsDCGroupEligibleForDR** tulajdonság $True értéke az eszközök feladatátvételéhez használható.</span><span class="sxs-lookup"><span data-stu-id="e14b0-114">Only the DCGroups that have a value of $True for the **IsDCGroupEligibleForDR** property can be used for device failover.</span></span>

## <span data-ttu-id="e14b0-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e14b0-115">PARAMETERS</span></span>

### <span data-ttu-id="e14b0-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e14b0-116">-DeviceId</span></span>
<span data-ttu-id="e14b0-117">Annak a StorSimple-eszköznek a példány-AZONOSÍTÓját adja meg, amelyen a parancsmagot futtatni szeretné.</span><span class="sxs-lookup"><span data-stu-id="e14b0-117">Specifies the instance ID of the StorSimple device on which to run the cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e14b0-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e14b0-118">-DeviceName</span></span>
<span data-ttu-id="e14b0-119">Annak a StorSimple-eszköznek a nevét adja meg, amelyen a parancsmagot futtatni szeretné.</span><span class="sxs-lookup"><span data-stu-id="e14b0-119">Specifies the name of the StorSimple device on which to run the cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e14b0-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="e14b0-120">-Profile</span></span>
<span data-ttu-id="e14b0-121">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="e14b0-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="e14b0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e14b0-122">CommonParameters</span></span>
<span data-ttu-id="e14b0-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e14b0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e14b0-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e14b0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e14b0-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e14b0-125">INPUTS</span></span>

## <span data-ttu-id="e14b0-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e14b0-126">OUTPUTS</span></span>

### <span data-ttu-id="e14b0-127">IList\<DataContainerGroup\></span><span class="sxs-lookup"><span data-stu-id="e14b0-127">IList\<DataContainerGroup\></span></span>
<span data-ttu-id="e14b0-128">Ez a parancsmag a **VolumeContainer** -csoportok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="e14b0-128">This cmdlet returns a list of **VolumeContainer** groups.</span></span>

## <span data-ttu-id="e14b0-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e14b0-129">NOTES</span></span>

## <span data-ttu-id="e14b0-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e14b0-130">RELATED LINKS</span></span>

[<span data-ttu-id="e14b0-131">Start-AzureStorSimpleDeviceFailoverJob</span><span class="sxs-lookup"><span data-stu-id="e14b0-131">Start-AzureStorSimpleDeviceFailoverJob</span></span>](./Start-AzureStorSimpleDeviceFailoverJob.md)

[<span data-ttu-id="e14b0-132">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="e14b0-132">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)


