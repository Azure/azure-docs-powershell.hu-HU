---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6715B3E8-6880-4B86-B831-41664766E12B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 026e06a0071084f07ed0b609b8b686e6cba44cc5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015650"
---
# <span data-ttu-id="cbc69-101">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="cbc69-101">Get-AzureDeploymentEvent</span></span>

## <span data-ttu-id="cbc69-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cbc69-102">SYNOPSIS</span></span>
<span data-ttu-id="cbc69-103">Információkat kaphat az Azure által kezdeményezett eseményekről, amelyek hatással vannak a virtuális gépekre és a Felhőbeli szolgáltatásokra.</span><span class="sxs-lookup"><span data-stu-id="cbc69-103">Gets information about events that Azure initiates that impact virtual machines and cloud services.</span></span>

## <span data-ttu-id="cbc69-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cbc69-104">SYNTAX</span></span>

### <span data-ttu-id="cbc69-105">GetDeploymentEventBySlot (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cbc69-105">GetDeploymentEventBySlot (Default)</span></span>
```
Get-AzureDeploymentEvent [-ServiceName] <String> [-StartTime] <DateTime> [-EndTime] <DateTime>
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cbc69-106">GetDeploymentEventByName</span><span class="sxs-lookup"><span data-stu-id="cbc69-106">GetDeploymentEventByName</span></span>
```
Get-AzureDeploymentEvent [-ServiceName] <String> [-StartTime] <DateTime> [-EndTime] <DateTime>
 [-DeploymentName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cbc69-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cbc69-107">DESCRIPTION</span></span>
<span data-ttu-id="cbc69-108">A **Get-AzureDeploymentEvent** parancsmag információkat nyújt az Azure által kezdeményezett eseményekről, amelyek hatással vannak a virtuális gépekre és a felhőalapú szolgáltatásokra.</span><span class="sxs-lookup"><span data-stu-id="cbc69-108">The **Get-AzureDeploymentEvent** cmdlet gets information regarding events that Azure initiates that impact virtual machines and cloud services.</span></span>
<span data-ttu-id="cbc69-109">Ezek az események magukban foglalják a tervezett karbantartási eseményeket.</span><span class="sxs-lookup"><span data-stu-id="cbc69-109">These events include planned maintenance events.</span></span>
<span data-ttu-id="cbc69-110">Ez a parancsmag azoknak az eseményeknek a listáját adja eredményül, amelyek meghatározzák a szerepkör-példányt vagy a virtuális gépet, az ütközés okát, valamint az esemény kezdési időpontját.</span><span class="sxs-lookup"><span data-stu-id="cbc69-110">This cmdlet returns a list of events that identify the role instance or virtual machine impacted, the reason for the impact, and the start time of the event.</span></span>

## <span data-ttu-id="cbc69-111">Példák</span><span class="sxs-lookup"><span data-stu-id="cbc69-111">EXAMPLES</span></span>

### <span data-ttu-id="cbc69-112">1:</span><span class="sxs-lookup"><span data-stu-id="cbc69-112">1:</span></span>
```
Get-AzureDeploymentEvent -DeploymentName "ConstosoDeployment" -ServiceName "ContosoService"
```

## <span data-ttu-id="cbc69-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cbc69-113">PARAMETERS</span></span>

### <span data-ttu-id="cbc69-114">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="cbc69-114">-DeploymentName</span></span>
<span data-ttu-id="cbc69-115">Annak a beállításnak a neve, amelyhez ez a parancsmag eseményeket kap.</span><span class="sxs-lookup"><span data-stu-id="cbc69-115">Specifies the name of the deployment for which this cmdlet gets events.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentEventByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc69-116">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="cbc69-116">-EndTime</span></span>
<span data-ttu-id="cbc69-117">Az ütemezett események befejezési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cbc69-117">Specifies the ending time for the scheduled events that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc69-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="cbc69-118">-InformationAction</span></span>
<span data-ttu-id="cbc69-119">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="cbc69-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cbc69-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="cbc69-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cbc69-121">Folytassa</span><span class="sxs-lookup"><span data-stu-id="cbc69-121">Continue</span></span>
- <span data-ttu-id="cbc69-122">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="cbc69-122">Ignore</span></span>
- <span data-ttu-id="cbc69-123">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="cbc69-123">Inquire</span></span>
- <span data-ttu-id="cbc69-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cbc69-124">SilentlyContinue</span></span>
- <span data-ttu-id="cbc69-125">állj</span><span class="sxs-lookup"><span data-stu-id="cbc69-125">Stop</span></span>
- <span data-ttu-id="cbc69-126">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="cbc69-126">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc69-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cbc69-127">-InformationVariable</span></span>
<span data-ttu-id="cbc69-128">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="cbc69-128">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc69-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="cbc69-129">-Profile</span></span>
<span data-ttu-id="cbc69-130">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="cbc69-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cbc69-131">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="cbc69-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cbc69-132">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="cbc69-132">-ServiceName</span></span>
<span data-ttu-id="cbc69-133">Annak a szolgáltatónak a neve, amelyhez a parancsmag ütemezett eseményeket kap.</span><span class="sxs-lookup"><span data-stu-id="cbc69-133">Specifies the name of the hosted service for which this cmdlet gets scheduled events.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbc69-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="cbc69-134">-Slot</span></span>
<span data-ttu-id="cbc69-135">Annak a központi példánynak a környezetét adja meg, amelyre a parancsmag ütemezett eseményeket kap.</span><span class="sxs-lookup"><span data-stu-id="cbc69-135">Specifies the environment of the deployment for which this cmdlet gets scheduled events.</span></span>
<span data-ttu-id="cbc69-136">Érvényes értékek: staging és termelés.</span><span class="sxs-lookup"><span data-stu-id="cbc69-136">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="cbc69-137">Az alapértelmezett érték a termelés.</span><span class="sxs-lookup"><span data-stu-id="cbc69-137">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentEventBySlot
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc69-138">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="cbc69-138">-StartTime</span></span>
<span data-ttu-id="cbc69-139">Az ütemezett események kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cbc69-139">Specifies the starting time for the scheduled events that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc69-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbc69-140">CommonParameters</span></span>
<span data-ttu-id="cbc69-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cbc69-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbc69-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbc69-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbc69-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbc69-143">INPUTS</span></span>

## <span data-ttu-id="cbc69-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbc69-144">OUTPUTS</span></span>

## <span data-ttu-id="cbc69-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cbc69-145">NOTES</span></span>

## <span data-ttu-id="cbc69-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbc69-146">RELATED LINKS</span></span>

[<span data-ttu-id="cbc69-147">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="cbc69-147">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)


