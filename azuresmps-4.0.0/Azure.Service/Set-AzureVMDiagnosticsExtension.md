---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A05B39BF-87EB-471E-9FCD-F7807CB46B4D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1aa7cff6d655bf33fa1a317516fda20237f6fc14
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016038"
---
# <span data-ttu-id="72983-101">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="72983-101">Set-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="72983-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72983-102">SYNOPSIS</span></span>
<span data-ttu-id="72983-103">Az Azure Diagnostics bővítmény beállítása virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="72983-103">Configures the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="72983-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72983-104">SYNTAX</span></span>

### <span data-ttu-id="72983-105">SetDiagnosticsExtension (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="72983-105">SetDiagnosticsExtension (Default)</span></span>
```
Set-AzureVMDiagnosticsExtension [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [[-Version] <String>] [-Disable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="72983-106">SetDiagnosticsWithReferenceExtension</span><span class="sxs-lookup"><span data-stu-id="72983-106">SetDiagnosticsWithReferenceExtension</span></span>
```
Set-AzureVMDiagnosticsExtension [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [[-Version] <String>] [-Disable] [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="72983-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="72983-107">DESCRIPTION</span></span>
<span data-ttu-id="72983-108">A **set-AzureVMDiagnosticsExtension** parancsmag a Microsoft Azure Diagnostics bővítményt egy virtuális gépen állítja be.</span><span class="sxs-lookup"><span data-stu-id="72983-108">The **Set-AzureVMDiagnosticsExtension** cmdlet configures the Microsoft Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="72983-109">Példák</span><span class="sxs-lookup"><span data-stu-id="72983-109">EXAMPLES</span></span>

### <span data-ttu-id="72983-110">Példa 1: virtuális gép létrehozása Azure Diagnostics bővítmény alkalmazásával</span><span class="sxs-lookup"><span data-stu-id="72983-110">Example 1: Create a virtual machine with Azure Diagnostics extension applied</span></span>
```
PS C:\> $VM = New-AzureVMConfig -Name $VM -InstanceSize Small -ImageName $VMImage
PS C:\> $VM = Add-AzureProvisioningConfig -VM $VM -AdminUsername $Username -Password $Password -Windows
PS C:\> $VM = Set-AzureVMDiagnosticsExtension -DiagnosticsConfigurationPath $Config_Path -Version "1.*" -VM $VM -StorageContext $Storage_Context
PS C:\> New-AzureVM -Location $Location -ServiceName $Service_Name -VM $VM
```

<span data-ttu-id="72983-111">Ezekkel a parancsokkal engedélyezzük az Azure Diagnostics bővítményt egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="72983-111">These commands enable the Azure Diagnostics extension on a virtual machine.</span></span>

### <span data-ttu-id="72983-112">2. példa: az Azure Diagnostics bővítmény engedélyezése meglévő virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="72983-112">Example 2: Enable an Azure Diagnostics extension on an existing virtual machine</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName $Service_Name -Name $VM_Name
PS C:\> $VM_Update = Set-AzureVMDiagnosticsExtension -DiagnosticsConfigurationPath $Config_Path -Version "1.*" -VM $VM -StorageContext $Storage_Context
PS C:\> Update-AzureVM -ServiceName $Service_Name -Name $VM_Name -VM $VM_Update.VM
```

<span data-ttu-id="72983-113">Az első parancs a **Get-AzureVM** parancsmagot használja a virtuális gép beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="72983-113">The first command uses the **Get-AzureVM** cmdlet to get a virtual machine.</span></span>

<span data-ttu-id="72983-114">A második parancs a **set-AzureVMDiagnosticsExtension** parancsmagot használja a virtuálisgép-konfiguráció frissítésére, hogy az Azure Diagnostics bővítmény szerepeljen benne.</span><span class="sxs-lookup"><span data-stu-id="72983-114">The second command uses the **Set-AzureVMDiagnosticsExtension** cmdlet to update the virtual machine configuration to include the Azure Diagnostics extension.</span></span>

<span data-ttu-id="72983-115">A végleges parancs alkalmazza a frissített konfigurációt a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="72983-115">The final command applies the updated configuration to the virtual machine.</span></span>

## <span data-ttu-id="72983-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72983-116">PARAMETERS</span></span>

### <span data-ttu-id="72983-117">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="72983-117">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="72983-118">A diagnosztikai konfiguráció elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="72983-118">Specifies a path for the diagnostics configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72983-119">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="72983-119">-Disable</span></span>
<span data-ttu-id="72983-120">Jelzi, hogy ez a parancsmag letiltja a diagnosztikai bővítményt a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="72983-120">Indicates that this cmdlet disables the diagnostics extension on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72983-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="72983-121">-InformationAction</span></span>
<span data-ttu-id="72983-122">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="72983-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="72983-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="72983-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="72983-124">Folytassa</span><span class="sxs-lookup"><span data-stu-id="72983-124">Continue</span></span>
- <span data-ttu-id="72983-125">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="72983-125">Ignore</span></span>
- <span data-ttu-id="72983-126">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="72983-126">Inquire</span></span>
- <span data-ttu-id="72983-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="72983-127">SilentlyContinue</span></span>
- <span data-ttu-id="72983-128">állj</span><span class="sxs-lookup"><span data-stu-id="72983-128">Stop</span></span>
- <span data-ttu-id="72983-129">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="72983-129">Suspend</span></span>

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

### <span data-ttu-id="72983-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="72983-130">-InformationVariable</span></span>
<span data-ttu-id="72983-131">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="72983-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="72983-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="72983-132">-Profile</span></span>
<span data-ttu-id="72983-133">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="72983-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="72983-134">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="72983-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="72983-135">-Hivatkozásnév</span><span class="sxs-lookup"><span data-stu-id="72983-135">-ReferenceName</span></span>
<span data-ttu-id="72983-136">A diagnosztikai bővítmény hivatkozási nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72983-136">Specifies the reference name for the diagnostics extension.</span></span>

```yaml
Type: String
Parameter Sets: SetDiagnosticsWithReferenceExtension
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72983-137">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="72983-137">-StorageAccountEndpoint</span></span>
<span data-ttu-id="72983-138">A tárolási fiók végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="72983-138">Specifies a storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72983-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="72983-139">-StorageAccountKey</span></span>
<span data-ttu-id="72983-140">A tárolási fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="72983-140">Specifies a storage account key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72983-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="72983-141">-StorageAccountName</span></span>
<span data-ttu-id="72983-142">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72983-142">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72983-143">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="72983-143">-StorageContext</span></span>
<span data-ttu-id="72983-144">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72983-144">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72983-145">-Verzió</span><span class="sxs-lookup"><span data-stu-id="72983-145">-Version</span></span>
<span data-ttu-id="72983-146">A kiterjesztés verziószámát adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="72983-146">Specifies the extension version as a string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72983-147">-VM</span><span class="sxs-lookup"><span data-stu-id="72983-147">-VM</span></span>
<span data-ttu-id="72983-148">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="72983-148">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72983-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72983-149">CommonParameters</span></span>
<span data-ttu-id="72983-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72983-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72983-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72983-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72983-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72983-152">INPUTS</span></span>

## <span data-ttu-id="72983-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72983-153">OUTPUTS</span></span>

## <span data-ttu-id="72983-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72983-154">NOTES</span></span>

## <span data-ttu-id="72983-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72983-155">RELATED LINKS</span></span>

[<span data-ttu-id="72983-156">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="72983-156">Get-AzureVMDiagnosticsExtension</span></span>](./Get-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="72983-157">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="72983-157">Remove-AzureVMDiagnosticsExtension</span></span>](./Remove-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="72983-158">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="72983-158">Update-AzureVM</span></span>](./Update-AzureVM.md)


