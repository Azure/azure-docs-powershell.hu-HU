---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 596B8A6F-D3C2-4170-BCD7-B7A1CDB656D8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ee767e1ba4c5008837e7cef98aafa4017465829
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016073"
---
# <span data-ttu-id="96e70-101">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="96e70-101">Restart-AzureVM</span></span>

## <span data-ttu-id="96e70-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96e70-102">SYNOPSIS</span></span>
<span data-ttu-id="96e70-103">Azure virtuális gép újraindítása.</span><span class="sxs-lookup"><span data-stu-id="96e70-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="96e70-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96e70-104">SYNTAX</span></span>

### <span data-ttu-id="96e70-105">RestartByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="96e70-105">RestartByName (Default)</span></span>
```
Restart-AzureVM [-Name] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="96e70-106">RedeployByName</span><span class="sxs-lookup"><span data-stu-id="96e70-106">RedeployByName</span></span>
```
Restart-AzureVM [-Name] <String> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="96e70-107">InitiateMaintenanceByName</span><span class="sxs-lookup"><span data-stu-id="96e70-107">InitiateMaintenanceByName</span></span>
```
Restart-AzureVM [-Name] <String> [-InitiateMaintenance] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="96e70-108">RestartInput</span><span class="sxs-lookup"><span data-stu-id="96e70-108">RestartInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="96e70-109">RedeployInput</span><span class="sxs-lookup"><span data-stu-id="96e70-109">RedeployInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="96e70-110">InitiateMaintenanceInput</span><span class="sxs-lookup"><span data-stu-id="96e70-110">InitiateMaintenanceInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-InitiateMaintenance] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="96e70-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="96e70-111">DESCRIPTION</span></span>
<span data-ttu-id="96e70-112">Az **Újraindítás – AzureVM** parancsmag az Azure Virtual Machine újraindítását kéri.</span><span class="sxs-lookup"><span data-stu-id="96e70-112">The **Restart-AzureVM** cmdlet requests a restart of an Azure virtual machine.</span></span>

## <span data-ttu-id="96e70-113">Példák</span><span class="sxs-lookup"><span data-stu-id="96e70-113">EXAMPLES</span></span>

### <span data-ttu-id="96e70-114">1. példa: virtuális gép újraindítása</span><span class="sxs-lookup"><span data-stu-id="96e70-114">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureVM -ServiceName "MyService01" -Name "MyVM"
```

<span data-ttu-id="96e70-115">Ez a parancs a Service01 nevű Azure szolgáltatásban futó VirtualMachine27-os virtuális gépet indítja el.</span><span class="sxs-lookup"><span data-stu-id="96e70-115">This command restarts the VirtualMachine27 virtual machine running in the Azure service named Service01.</span></span>

### <span data-ttu-id="96e70-116">2. példa: virtuális gép újraindítása virtuálisgép-objektum használatával</span><span class="sxs-lookup"><span data-stu-id="96e70-116">Example 2: Restart a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "MyService01" -Name "VirtualMachine27" | Restart-AzureVM
```

<span data-ttu-id="96e70-117">Ez a parancs beolvassa a MyVM nevű virtuális gép objektumát, majd újraindul.</span><span class="sxs-lookup"><span data-stu-id="96e70-117">This command retrieves the virtual machine object for the virtual machine named MyVM and then restarts it.</span></span>

## <span data-ttu-id="96e70-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96e70-118">PARAMETERS</span></span>

### <span data-ttu-id="96e70-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="96e70-119">-InformationAction</span></span>
<span data-ttu-id="96e70-120">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="96e70-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="96e70-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="96e70-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="96e70-122">Folytassa</span><span class="sxs-lookup"><span data-stu-id="96e70-122">Continue</span></span>
- <span data-ttu-id="96e70-123">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="96e70-123">Ignore</span></span>
- <span data-ttu-id="96e70-124">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="96e70-124">Inquire</span></span>
- <span data-ttu-id="96e70-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="96e70-125">SilentlyContinue</span></span>
- <span data-ttu-id="96e70-126">állj</span><span class="sxs-lookup"><span data-stu-id="96e70-126">Stop</span></span>
- <span data-ttu-id="96e70-127">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="96e70-127">Suspend</span></span>

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

### <span data-ttu-id="96e70-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="96e70-128">-InformationVariable</span></span>
<span data-ttu-id="96e70-129">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="96e70-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="96e70-130">-InitiateMaintenance</span><span class="sxs-lookup"><span data-stu-id="96e70-130">-InitiateMaintenance</span></span>
<span data-ttu-id="96e70-131">Karbantartás kezdeményezése a virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="96e70-131">Initiate Maintenance on the Virtual Machine</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: InitiateMaintenanceByName, InitiateMaintenanceInput
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e70-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="96e70-132">-Name</span></span>
<span data-ttu-id="96e70-133">Az újraindítani kívánt virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="96e70-133">Specifies the name of the virtual machine to restart.</span></span>

```yaml
Type: String
Parameter Sets: RestartByName, RedeployByName, InitiateMaintenanceByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96e70-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="96e70-134">-Profile</span></span>
<span data-ttu-id="96e70-135">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="96e70-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="96e70-136">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="96e70-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="96e70-137">-Redeploy</span><span class="sxs-lookup"><span data-stu-id="96e70-137">-Redeploy</span></span>
<span data-ttu-id="96e70-138">Azt jelzi, hogy a parancsmag áttelepíti a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="96e70-138">Indicates that the cmdlet redeploys the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RedeployByName, RedeployInput
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e70-139">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="96e70-139">-ServiceName</span></span>
<span data-ttu-id="96e70-140">Annak az Azure-szolgáltatásnak a neve, amely az újraindításhoz használt virtuális gépet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="96e70-140">Specifies the name of the Azure service that contains the virtual machine to restart.</span></span>

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

### <span data-ttu-id="96e70-141">-VM</span><span class="sxs-lookup"><span data-stu-id="96e70-141">-VM</span></span>
<span data-ttu-id="96e70-142">Megadja azt a virtuálisgép-objektumot, amely azonosítja a virtuális gépet az újraindításhoz.</span><span class="sxs-lookup"><span data-stu-id="96e70-142">Specifies a virtual machine object that identifies the virtual machine to restart.</span></span>

```yaml
Type: PersistentVM
Parameter Sets: RestartInput, RedeployInput, InitiateMaintenanceInput
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96e70-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96e70-143">CommonParameters</span></span>
<span data-ttu-id="96e70-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96e70-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96e70-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96e70-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96e70-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96e70-146">INPUTS</span></span>

## <span data-ttu-id="96e70-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96e70-147">OUTPUTS</span></span>

## <span data-ttu-id="96e70-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96e70-148">NOTES</span></span>

## <span data-ttu-id="96e70-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96e70-149">RELATED LINKS</span></span>

[<span data-ttu-id="96e70-150">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="96e70-150">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="96e70-151">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="96e70-151">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="96e70-152">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="96e70-152">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="96e70-153">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="96e70-153">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="96e70-154">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="96e70-154">Update-AzureVM</span></span>](./Update-AzureVM.md)


