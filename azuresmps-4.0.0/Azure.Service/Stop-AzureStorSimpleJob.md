---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A1E143A8-70F2-4158-9A10-F2082AD62A73
online version: ''
schema: 2.0.0
ms.openlocfilehash: 371291f4bd33809bc2f5880e4380c448219ed37a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016012"
---
# <span data-ttu-id="92276-101">Stop-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="92276-101">Stop-AzureStorSimpleJob</span></span>

## <span data-ttu-id="92276-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92276-102">SYNOPSIS</span></span>
<span data-ttu-id="92276-103">Leállít egy StorSimple-feladatot.</span><span class="sxs-lookup"><span data-stu-id="92276-103">Stops a StorSimple job.</span></span>

## <span data-ttu-id="92276-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92276-104">SYNTAX</span></span>

```
Stop-AzureStorSimpleJob -InstanceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="92276-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="92276-105">DESCRIPTION</span></span>
<span data-ttu-id="92276-106">A **stop-AzureStorSimpleJob** parancsmag egy folyamatban lévő StorSimple-feladatot leáll.</span><span class="sxs-lookup"><span data-stu-id="92276-106">The **Stop-AzureStorSimpleJob** cmdlet stops an on-going StorSimple job.</span></span>
<span data-ttu-id="92276-107">A munkafolyamatokat a példány-AZONOSÍTÓk vagy a feladatnév megadásával is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="92276-107">You can specify a jobs by supplying an instance ID or a job name.</span></span>

## <span data-ttu-id="92276-108">Példák</span><span class="sxs-lookup"><span data-stu-id="92276-108">EXAMPLES</span></span>

### <span data-ttu-id="92276-109">1. példa: a feladatok leállítása egy eszközön</span><span class="sxs-lookup"><span data-stu-id="92276-109">Example 1: Stop jobs for a device</span></span>
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" | Stop-AzureStorSimpleJob -Force
```

<span data-ttu-id="92276-110">Ez a parancs a **Get-AzureStorSimpleJob** parancsmag használatával kapja meg a Device07 nevű eszköz munkahelyeit.</span><span class="sxs-lookup"><span data-stu-id="92276-110">This command gets the jobs for the device named Device07, by using the **Get-AzureStorSimpleJob** cmdlet.</span></span>
<span data-ttu-id="92276-111">A parancs a pipeline operátorral továbbítja a feladatokat az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="92276-111">The command passes the jobs to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="92276-112">Az aktuális parancsmag megszünteti azokat a feladatokat, amelyekre a parancs a parancsot átadja.</span><span class="sxs-lookup"><span data-stu-id="92276-112">The current cmdlet stops any jobs that the command passes to it.</span></span>
<span data-ttu-id="92276-113">A parancs az *erő* paramétert adja meg, ezért a feladat leállítása előtt nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="92276-113">The command specifies the *Force* parameter, and, so, it does not prompt you for confirmation before it stops a job.</span></span>

### <span data-ttu-id="92276-114">2. példa: adott feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="92276-114">Example 2: Stop a specific job</span></span>
```
PS C:\>Stop-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d" -Force
```

<span data-ttu-id="92276-115">Ez a parancs leállítja a megadott példány-azonosítót tartalmazó munkát.</span><span class="sxs-lookup"><span data-stu-id="92276-115">This command stops the job that has the specified instance ID.</span></span>

## <span data-ttu-id="92276-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92276-116">PARAMETERS</span></span>

### <span data-ttu-id="92276-117">-Force</span><span class="sxs-lookup"><span data-stu-id="92276-117">-Force</span></span>
<span data-ttu-id="92276-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="92276-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92276-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="92276-119">-InstanceId</span></span>
<span data-ttu-id="92276-120">A leállításhoz adja meg az eszköz feladatának AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="92276-120">Specifies the ID of the device job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92276-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="92276-121">-Profile</span></span>
<span data-ttu-id="92276-122">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="92276-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="92276-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92276-123">CommonParameters</span></span>
<span data-ttu-id="92276-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92276-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92276-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92276-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92276-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92276-126">INPUTS</span></span>

### <span data-ttu-id="92276-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="92276-127">None</span></span>

## <span data-ttu-id="92276-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92276-128">OUTPUTS</span></span>

### <span data-ttu-id="92276-129">DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="92276-129">DeviceJobDetails</span></span>
<span data-ttu-id="92276-130">Ez a parancsmag azokat a **DeviceJob** részletezi, amelyekre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="92276-130">This cmdlet gets details of the **DeviceJob** that this cmdlet stops.</span></span>

## <span data-ttu-id="92276-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92276-131">NOTES</span></span>

## <span data-ttu-id="92276-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92276-132">RELATED LINKS</span></span>

[<span data-ttu-id="92276-133">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="92276-133">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


