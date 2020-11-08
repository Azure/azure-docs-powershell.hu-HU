---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4F347DD1-907C-47DB-8F1D-636DE031A56A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e01265cf3db8a0dc3fd9d74a4a263a20965b10fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015741"
---
# <span data-ttu-id="ae0f7-101">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ae0f7-101">Stop-AzureVM</span></span>

## <span data-ttu-id="ae0f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae0f7-102">SYNOPSIS</span></span>
<span data-ttu-id="ae0f7-103">Egy Azure Virtual Machine leállása.</span><span class="sxs-lookup"><span data-stu-id="ae0f7-103">Shuts down an Azure virtual machine.</span></span>

## <span data-ttu-id="ae0f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae0f7-104">SYNTAX</span></span>

### <span data-ttu-id="ae0f7-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ae0f7-105">ByName (Default)</span></span>
```
Stop-AzureVM [-Name] <String[]> [-StayProvisioned] [-Force] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ae0f7-106">Beviteli</span><span class="sxs-lookup"><span data-stu-id="ae0f7-106">Input</span></span>
```
Stop-AzureVM -VM <IPersistentVM[]> [-StayProvisioned] [-Force] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae0f7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae0f7-107">DESCRIPTION</span></span>
<span data-ttu-id="ae0f7-108">A **stop-AzureVM** parancsmag leállítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="ae0f7-108">The **Stop-AzureVM** cmdlet shuts down a virtual machine.</span></span>

## <span data-ttu-id="ae0f7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ae0f7-109">EXAMPLES</span></span>

### <span data-ttu-id="ae0f7-110">Példa 1: virtuális gép leállítása</span><span class="sxs-lookup"><span data-stu-id="ae0f7-110">Example 1: Shut down a virtual machine</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM"
```

<span data-ttu-id="ae0f7-111">Ez a parancs leállítja a megadott szolgáltatás által használt virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="ae0f7-111">This command shuts down a virtual machine that the specified service contains.</span></span>

### <span data-ttu-id="ae0f7-112">2. példa: virtuális gép leállítása egy virtuálisgép-objektum segítségével</span><span class="sxs-lookup"><span data-stu-id="ae0f7-112">Example 2: Shut down a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "MyVM" | Stop-AzureVM
```

<span data-ttu-id="ae0f7-113">Ez a parancs leállítja azt a virtuális gépet, amelyet a megadott szolgáltatás tartalmaz, a **beolvasás AzureVM** visszaadó virtuálisgép-objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="ae0f7-113">This command shuts down a virtual machine that the specified service contains, by using the virtual machine object that **Get-AzureVM** returns.</span></span>

### <span data-ttu-id="ae0f7-114">3. példa: állítsa le a VM-et, és őrizze meg a VM kiépített változatát</span><span class="sxs-lookup"><span data-stu-id="ae0f7-114">Example 3: Shut down a VM and keep the VM provisioned</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -StayProvisioned
```

<span data-ttu-id="ae0f7-115">Ez a parancs leállítja azt a virtuális gépet, amelyet a megadott szolgáltatás tartalmaz, és kiépített állapotban tartja.</span><span class="sxs-lookup"><span data-stu-id="ae0f7-115">This command shuts down a virtual machine that the specified service contains, and keeps it provisioned.</span></span>

### <span data-ttu-id="ae0f7-116">4. példa: állítsa le a VM-et, és engedélyezze az utolsó VM kiosztását a központi üzembe helyezésben.</span><span class="sxs-lookup"><span data-stu-id="ae0f7-116">Example 4: Shut down a VM and allow deallocation of the last VM in the deployment</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -Force
```

<span data-ttu-id="ae0f7-117">Ez a parancs leállítja azt a virtuális gépet, amelyet a megadott szolgáltatás tartalmaz, és lehetővé teszi az utolsó virtuális gép deallokációját a központi üzembe helyezéshez.</span><span class="sxs-lookup"><span data-stu-id="ae0f7-117">This command shuts down a virtual machine that the specified service contains and allows deallocation of the last virtual machine in the deployment.</span></span>

### <span data-ttu-id="ae0f7-118">Példa 5: több VMs kikapcsolása</span><span class="sxs-lookup"><span data-stu-id="ae0f7-118">Example 5: Shut down multiple VMs</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "PSTestService" -Name "*" -Force
```

<span data-ttu-id="ae0f7-119">Ez a parancs több olyan virtuális gépet leállít le, amelyeket a megadott szolgáltatás tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="ae0f7-119">This command shuts down multiple virtual machines that the specified service contains.</span></span>

## <span data-ttu-id="ae0f7-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae0f7-120">PARAMETERS</span></span>

### <span data-ttu-id="ae0f7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ae0f7-121">-Force</span></span>
<span data-ttu-id="ae0f7-122">Azt adja meg, hogy engedélyezi-e az utolsó virtuális gép deallokációját egy központi példányban.</span><span class="sxs-lookup"><span data-stu-id="ae0f7-122">Specifies whether to allow the deallocation of the last virtual machine in a deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae0f7-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ae0f7-123">-InformationAction</span></span>
<span data-ttu-id="ae0f7-124">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="ae0f7-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ae0f7-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ae0f7-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae0f7-126">Folytassa</span><span class="sxs-lookup"><span data-stu-id="ae0f7-126">Continue</span></span>
- <span data-ttu-id="ae0f7-127">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="ae0f7-127">Ignore</span></span>
- <span data-ttu-id="ae0f7-128">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="ae0f7-128">Inquire</span></span>
- <span data-ttu-id="ae0f7-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ae0f7-129">SilentlyContinue</span></span>
- <span data-ttu-id="ae0f7-130">állj</span><span class="sxs-lookup"><span data-stu-id="ae0f7-130">Stop</span></span>
- <span data-ttu-id="ae0f7-131">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="ae0f7-131">Suspend</span></span>

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

### <span data-ttu-id="ae0f7-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ae0f7-132">-InformationVariable</span></span>
<span data-ttu-id="ae0f7-133">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="ae0f7-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ae0f7-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ae0f7-134">-Name</span></span>
<span data-ttu-id="ae0f7-135">A leállításhoz a virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae0f7-135">Specifies the name of the virtual machine to shut down.</span></span>

<span data-ttu-id="ae0f7-136">A helyettesítő karakterrel több virtuális gépet aszinkron módon állíthat be.</span><span class="sxs-lookup"><span data-stu-id="ae0f7-136">Use the wildcard character to stop multiple virtual machines asynchronously.</span></span>
<span data-ttu-id="ae0f7-137">A helyettesítő karakterekkel ez a parancsmag a leállítási szerepkörök https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx műveletét hívja le ( https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx) a leállítási szerepkör https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx művelete helyett https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx) ).</span><span class="sxs-lookup"><span data-stu-id="ae0f7-137">With a wildcard character, this cmdlet calls the Shutdown Roleshttps://msdn.microsoft.com/en-us/library/azure/dn469421.aspx operation (https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx), instead of the Shutdown Rolehttps://msdn.microsoft.com/en-us/library/azure/jj157195.aspx operation (https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx).</span></span>

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae0f7-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="ae0f7-138">-Profile</span></span>
<span data-ttu-id="ae0f7-139">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ae0f7-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ae0f7-140">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ae0f7-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ae0f7-141">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="ae0f7-141">-ServiceName</span></span>
<span data-ttu-id="ae0f7-142">Annak a virtuális gépet tartalmazó Azure-szolgáltatásnak a neve, amelyről le kell állítani.</span><span class="sxs-lookup"><span data-stu-id="ae0f7-142">Specifies the name of the Azure service that contains the virtual machine to shut down.</span></span>

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

### <span data-ttu-id="ae0f7-143">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="ae0f7-143">-StayProvisioned</span></span>
<span data-ttu-id="ae0f7-144">Megadja, hogy ez a parancsmag a virtuális gépet kiépítve tartja.</span><span class="sxs-lookup"><span data-stu-id="ae0f7-144">Specifies that this cmdlet keeps the virtual machine provisioned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae0f7-145">-VM</span><span class="sxs-lookup"><span data-stu-id="ae0f7-145">-VM</span></span>
<span data-ttu-id="ae0f7-146">Olyan virtuálisgép-objektumot ad meg, amely azonosítja a virtuális gépet a leállításhoz.</span><span class="sxs-lookup"><span data-stu-id="ae0f7-146">Specifies a virtual machine object that identifies the virtual machine to shut down.</span></span>

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae0f7-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae0f7-147">CommonParameters</span></span>
<span data-ttu-id="ae0f7-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae0f7-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae0f7-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae0f7-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae0f7-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae0f7-150">INPUTS</span></span>

## <span data-ttu-id="ae0f7-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae0f7-151">OUTPUTS</span></span>

## <span data-ttu-id="ae0f7-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae0f7-152">NOTES</span></span>

## <span data-ttu-id="ae0f7-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae0f7-153">RELATED LINKS</span></span>

[<span data-ttu-id="ae0f7-154">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ae0f7-154">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="ae0f7-155">Új – AzureVM</span><span class="sxs-lookup"><span data-stu-id="ae0f7-155">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="ae0f7-156">Újraindítás – AzureVM</span><span class="sxs-lookup"><span data-stu-id="ae0f7-156">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="ae0f7-157">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ae0f7-157">Start-AzureVM</span></span>](./Start-AzureVM.md)


