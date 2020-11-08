---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BBA0D5D3-29A5-4E00-9075-702E2F81CA52
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcff7873042d9f7a07eee26f93312c8690e16416
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016547"
---
# <span data-ttu-id="a317f-101">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a317f-101">Get-AzureVM</span></span>

## <span data-ttu-id="a317f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a317f-102">SYNOPSIS</span></span>
<span data-ttu-id="a317f-103">Beolvassa az adatokat egy vagy több Azure virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="a317f-103">Retrieves information from one or more Azure virtual machines.</span></span>

## <span data-ttu-id="a317f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a317f-104">SYNTAX</span></span>

### <span data-ttu-id="a317f-105">ListAllVMs (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a317f-105">ListAllVMs (Default)</span></span>
```
Get-AzureVM [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a317f-106">GetVMByServiceAndVMName</span><span class="sxs-lookup"><span data-stu-id="a317f-106">GetVMByServiceAndVMName</span></span>
```
Get-AzureVM [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a317f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a317f-107">DESCRIPTION</span></span>
<span data-ttu-id="a317f-108">A **Get-AzureVM** parancsmag információkat keres az Azure-ban futó virtuális gépekről.</span><span class="sxs-lookup"><span data-stu-id="a317f-108">The **Get-AzureVM** cmdlet retrieves information about virtual machines running in Azure.</span></span>
<span data-ttu-id="a317f-109">Egy olyan objektumot ad eredményül, amely egy adott virtuális gépen információt ad, vagy ha nincs megadva virtuális gép, az aktuális előfizetéshez megadott szolgáltatásban lévő összes virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="a317f-109">It returns an object with information on a specific virtual machine, or if no virtual machine is specified, for all the virtual machines in the specified service of the current subscription.</span></span>

## <span data-ttu-id="a317f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a317f-110">EXAMPLES</span></span>

### <span data-ttu-id="a317f-111">Példa 1: adatok beolvasása egy adott virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="a317f-111">Example 1: Retrieve information on a specified virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "VirtualMachine02"
```

<span data-ttu-id="a317f-112">Ez a parancs egy olyan objektumot ad eredményül, amely a ContosoService01 felhőben futó VirtualMachine02 virtuális gépén található.</span><span class="sxs-lookup"><span data-stu-id="a317f-112">This command returns an object with information on the VirtualMachine02 virtual machine running in the ContosoService01 cloud service.</span></span>

### <span data-ttu-id="a317f-113">2. példa: adatok beolvasása az összes virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="a317f-113">Example 2: Retrieve information on all virtual machines</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"
```

<span data-ttu-id="a317f-114">Ez a parancs a ContosoService01 felhőben futó összes virtuális gépen információt tartalmazó lista-objektumot keres.</span><span class="sxs-lookup"><span data-stu-id="a317f-114">This command retrieves a list object with information on all of the virtual machines running in the ContosoService01 cloud service.</span></span>

### <span data-ttu-id="a317f-115">3. példa: a virtuális gép állapotait tartalmazó táblázat megjelenítése</span><span class="sxs-lookup"><span data-stu-id="a317f-115">Example 3: Display a table of virtual machine statuses</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"  | Format-Table AutoSize -Property "Name",@{Expression={$_.InstanceUpgradeDomain};Label="UpgDom";Align="Right"},"InstanceStatus"
```

<span data-ttu-id="a317f-116">Ez a parancs megjeleníti a ContosoService01 szolgáltatásban futó virtuális gépeket, azok frissítési tartományát, valamint az egyes virtuális gépek pillanatnyi állapotát.</span><span class="sxs-lookup"><span data-stu-id="a317f-116">This command displays a table showing the virtual machines running on the ContosoService01 service, their Upgrade Domain, and the current status of each virtual machine.</span></span>

## <span data-ttu-id="a317f-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a317f-117">PARAMETERS</span></span>

### <span data-ttu-id="a317f-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a317f-118">-InformationAction</span></span>
<span data-ttu-id="a317f-119">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="a317f-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a317f-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a317f-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a317f-121">Folytassa</span><span class="sxs-lookup"><span data-stu-id="a317f-121">Continue</span></span>
- <span data-ttu-id="a317f-122">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="a317f-122">Ignore</span></span>
- <span data-ttu-id="a317f-123">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="a317f-123">Inquire</span></span>
- <span data-ttu-id="a317f-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a317f-124">SilentlyContinue</span></span>
- <span data-ttu-id="a317f-125">állj</span><span class="sxs-lookup"><span data-stu-id="a317f-125">Stop</span></span>
- <span data-ttu-id="a317f-126">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="a317f-126">Suspend</span></span>

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

### <span data-ttu-id="a317f-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a317f-127">-InformationVariable</span></span>
<span data-ttu-id="a317f-128">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="a317f-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a317f-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a317f-129">-Name</span></span>
<span data-ttu-id="a317f-130">Annak a virtuális gépnek a neve, amelyhez információt szeretne beolvasni.</span><span class="sxs-lookup"><span data-stu-id="a317f-130">Specifies the name of the virtual machine for which to retrieve information.</span></span>
<span data-ttu-id="a317f-131">Ha ez a paraméter nincs megadva, a parancsmag egy lista objektumot ad eredményül, amely a megadott szolgáltatás összes virtuális gépre vonatkozó információt tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="a317f-131">If this parameter is not provided, the cmdlet returns a list object with information about all the virtual machines in the specified service.</span></span>

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a317f-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="a317f-132">-Profile</span></span>
<span data-ttu-id="a317f-133">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="a317f-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a317f-134">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="a317f-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a317f-135">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="a317f-135">-ServiceName</span></span>
<span data-ttu-id="a317f-136">Annak a felhőalapú szolgáltatásnak a nevét adja meg, amelyből vissza szeretné adni a virtuálisgép-információkat.</span><span class="sxs-lookup"><span data-stu-id="a317f-136">Specifies the name of the cloud service for which to return virtual machine information.</span></span>

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a317f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a317f-137">CommonParameters</span></span>
<span data-ttu-id="a317f-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a317f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a317f-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a317f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a317f-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a317f-140">INPUTS</span></span>

## <span data-ttu-id="a317f-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a317f-141">OUTPUTS</span></span>

## <span data-ttu-id="a317f-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a317f-142">NOTES</span></span>

## <span data-ttu-id="a317f-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a317f-143">RELATED LINKS</span></span>

[<span data-ttu-id="a317f-144">Új – AzureVM</span><span class="sxs-lookup"><span data-stu-id="a317f-144">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="a317f-145">Új – AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="a317f-145">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="a317f-146">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a317f-146">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="a317f-147">Újraindítás – AzureVM</span><span class="sxs-lookup"><span data-stu-id="a317f-147">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="a317f-148">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a317f-148">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="a317f-149">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a317f-149">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="a317f-150">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a317f-150">Update-AzureVM</span></span>](./Update-AzureVM.md)


