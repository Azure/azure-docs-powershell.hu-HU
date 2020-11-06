---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: c3a146b99119ab94bf98176d202cda52e1dc5704
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499023"
---
# <span data-ttu-id="e83a2-101">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e83a2-101">Set-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="e83a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e83a2-102">SYNOPSIS</span></span>
<span data-ttu-id="e83a2-103">Egy virtuális gépen az Azure SQL Server-bővítményt állítja be.</span><span class="sxs-lookup"><span data-stu-id="e83a2-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e83a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e83a2-104">SYNTAX</span></span>

```
Set-AzureRmVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="e83a2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e83a2-105">DESCRIPTION</span></span>
<span data-ttu-id="e83a2-106">A **set-AzureRmVMSqlServerExtension** parancsmag egy virtuális gépen beállítja a AzureSQL Server bővítményt.</span><span class="sxs-lookup"><span data-stu-id="e83a2-106">The **Set-AzureRmVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="e83a2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e83a2-107">EXAMPLES</span></span>

### <span data-ttu-id="e83a2-108">1. példa: automatikus javítási beállítások megadása virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="e83a2-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzureRmVM
```

<span data-ttu-id="e83a2-109">Az első parancs a **New-AzureVMSqlServerAutoPatchingConfig** parancsmag segítségével hoz létre konfigurációs objektumot.</span><span class="sxs-lookup"><span data-stu-id="e83a2-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="e83a2-110">A parancs a $AutoPatchingConfig változóban tárolja a konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="e83a2-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>

<span data-ttu-id="e83a2-111">A második parancs a VirtualMachine11 nevű virtuális gépet a Service02 nevű szolgáltatáson keresztül kapja meg az Get-AzureRmVM parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="e83a2-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="e83a2-112">A parancs a csővezeték-kezelő használatával továbbítja az objektumot az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="e83a2-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="e83a2-113">Az aktuális parancsmag a virtuális gép $AutoPatchingConfig automatikus javítási beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="e83a2-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="e83a2-114">A parancs átadja a virtuális gépet az Update-AzureRmVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="e83a2-114">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="e83a2-115">2. példa: automatikus biztonsági mentési beállítások megadása virtuális számítógépen</span><span class="sxs-lookup"><span data-stu-id="e83a2-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzureRmVM
```

<span data-ttu-id="e83a2-116">Az első parancs a **New-AzureVMSqlServerAutoBackupConfig** parancsmag segítségével hoz létre konfigurációs objektumot.</span><span class="sxs-lookup"><span data-stu-id="e83a2-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="e83a2-117">A parancs a $AutoBackupConfig változóban tárolja a konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="e83a2-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>

<span data-ttu-id="e83a2-118">A második parancs megkapja a VirtualMachine11 nevű virtuális gépet a Service02 nevű szolgáltatásban, majd átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="e83a2-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>

<span data-ttu-id="e83a2-119">A jelenlegi parancsmag a virtuális gép $AutoBackupConfigban található automatikus biztonsági mentési beállításokat állítja be.</span><span class="sxs-lookup"><span data-stu-id="e83a2-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="e83a2-120">A parancs átadja a virtuális gépet az Update-AzureRmVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="e83a2-120">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="e83a2-121">3. példa: SQL Server-bővítmény letiltása virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="e83a2-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Disable
```

<span data-ttu-id="e83a2-122">Ez a parancs a Service03 nevű virtuális gépet kapja, majd átadja az aktuális parancsmagnak a VirtualMachine08.</span><span class="sxs-lookup"><span data-stu-id="e83a2-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="e83a2-123">A parancs letiltja az SQL Server Virtual Machine bővítményt a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="e83a2-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="e83a2-124">4. példa: az SQL Server-bővítmények eltávolítása egy adott virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="e83a2-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Uninstall
```

<span data-ttu-id="e83a2-125">Ez a parancs a Service03 nevű virtuális gépet kapja, majd átadja az aktuális parancsmagnak a VirtualMachine08.</span><span class="sxs-lookup"><span data-stu-id="e83a2-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="e83a2-126">A parancs eltávolítja az SQL Server Virtual Machine bővítményt a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="e83a2-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="e83a2-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e83a2-127">PARAMETERS</span></span>

### <span data-ttu-id="e83a2-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="e83a2-128">-AutoBackupSettings</span></span>
<span data-ttu-id="e83a2-129">Az automatikus SQL Server biztonsági mentési beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="e83a2-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="e83a2-130">**AutoBackupSettings** -objektum létrehozásához használja az New-AzureVMSqlServerAutoBackupConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e83a2-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

```yaml
Type: AutoBackupSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e83a2-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="e83a2-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="e83a2-132">Az automatikus SQL Server-javítás beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="e83a2-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="e83a2-133">**AutoPatchingSettings** -objektum létrehozásához használja az New-AzureVMSqlServerAutoPatchingConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e83a2-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

```yaml
Type: AutoPatchingSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e83a2-134">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="e83a2-134">-KeyVaultCredentialSettings</span></span>
```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e83a2-135">-Hely</span><span class="sxs-lookup"><span data-stu-id="e83a2-135">-Location</span></span>
<span data-ttu-id="e83a2-136">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e83a2-136">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e83a2-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e83a2-137">-Name</span></span>
<span data-ttu-id="e83a2-138">Annak az SQL Server-kiszolgálónak a nevét adja meg, amely a kiterjesztést adja.</span><span class="sxs-lookup"><span data-stu-id="e83a2-138">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e83a2-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e83a2-139">-ResourceGroupName</span></span>
<span data-ttu-id="e83a2-140">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e83a2-140">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e83a2-141">-Verzió</span><span class="sxs-lookup"><span data-stu-id="e83a2-141">-Version</span></span>
<span data-ttu-id="e83a2-142">Az SQL Server-bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e83a2-142">Specifies the version of the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e83a2-143">-VMName</span><span class="sxs-lookup"><span data-stu-id="e83a2-143">-VMName</span></span>
<span data-ttu-id="e83a2-144">Annak a virtuális gépnek a neve, amelyen a parancsmag az SQL Server-bővítményt állítja be.</span><span class="sxs-lookup"><span data-stu-id="e83a2-144">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e83a2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e83a2-145">CommonParameters</span></span>
<span data-ttu-id="e83a2-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e83a2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e83a2-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e83a2-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e83a2-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e83a2-148">INPUTS</span></span>

### <span data-ttu-id="e83a2-149">Nincs</span><span class="sxs-lookup"><span data-stu-id="e83a2-149">None</span></span>
<span data-ttu-id="e83a2-150">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e83a2-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e83a2-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e83a2-151">OUTPUTS</span></span>

## <span data-ttu-id="e83a2-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e83a2-152">NOTES</span></span>

## <span data-ttu-id="e83a2-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e83a2-153">RELATED LINKS</span></span>

[<span data-ttu-id="e83a2-154">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e83a2-154">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="e83a2-155">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e83a2-155">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="e83a2-156">Új – AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="e83a2-156">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="e83a2-157">Új – AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="e83a2-157">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="e83a2-158">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e83a2-158">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="e83a2-159">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e83a2-159">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


