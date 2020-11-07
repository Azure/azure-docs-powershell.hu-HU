---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 4093e236f84d7587586ba30c8bd4653c4ba7358f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844194"
---
# <span data-ttu-id="64447-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="64447-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="64447-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64447-102">SYNOPSIS</span></span>
<span data-ttu-id="64447-103">Egy virtuális gépen az Azure SQL Server-bővítményt állítja be.</span><span class="sxs-lookup"><span data-stu-id="64447-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="64447-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64447-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64447-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="64447-105">DESCRIPTION</span></span>
<span data-ttu-id="64447-106">A **set-AzVMSqlServerExtension** parancsmag egy virtuális gépen beállítja a AzureSQL Server bővítményt.</span><span class="sxs-lookup"><span data-stu-id="64447-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="64447-107">Példák</span><span class="sxs-lookup"><span data-stu-id="64447-107">EXAMPLES</span></span>

### <span data-ttu-id="64447-108">1. példa: automatikus javítási beállítások megadása virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="64447-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="64447-109">Az első parancs a **New-AzureVMSqlServerAutoPatchingConfig** parancsmag segítségével hoz létre konfigurációs objektumot.</span><span class="sxs-lookup"><span data-stu-id="64447-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="64447-110">A parancs a $AutoPatchingConfig változóban tárolja a konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="64447-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>

<span data-ttu-id="64447-111">A második parancs a VirtualMachine11 nevű virtuális gépet a Service02 nevű szolgáltatáson keresztül kapja meg az Get-AzVM parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="64447-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="64447-112">A parancs a csővezeték-kezelő használatával továbbítja az objektumot az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="64447-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="64447-113">Az aktuális parancsmag a virtuális gép $AutoPatchingConfig automatikus javítási beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="64447-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="64447-114">A parancs átadja a virtuális gépet az Update-AzVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="64447-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="64447-115">2. példa: automatikus biztonsági mentési beállítások megadása virtuális számítógépen</span><span class="sxs-lookup"><span data-stu-id="64447-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="64447-116">Az első parancs a **New-AzureVMSqlServerAutoBackupConfig** parancsmag segítségével hoz létre konfigurációs objektumot.</span><span class="sxs-lookup"><span data-stu-id="64447-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="64447-117">A parancs a $AutoBackupConfig változóban tárolja a konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="64447-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>

<span data-ttu-id="64447-118">A második parancs megkapja a VirtualMachine11 nevű virtuális gépet a Service02 nevű szolgáltatásban, majd átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="64447-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>

<span data-ttu-id="64447-119">A jelenlegi parancsmag a virtuális gép $AutoBackupConfigban található automatikus biztonsági mentési beállításokat állítja be.</span><span class="sxs-lookup"><span data-stu-id="64447-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="64447-120">A parancs átadja a virtuális gépet az Update-AzVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="64447-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="64447-121">3. példa: SQL Server-bővítmény letiltása virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="64447-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="64447-122">Ez a parancs a Service03 nevű virtuális gépet kapja, majd átadja az aktuális parancsmagnak a VirtualMachine08.</span><span class="sxs-lookup"><span data-stu-id="64447-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="64447-123">A parancs letiltja az SQL Server Virtual Machine bővítményt a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="64447-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="64447-124">4. példa: az SQL Server-bővítmények eltávolítása egy adott virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="64447-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="64447-125">Ez a parancs a Service03 nevű virtuális gépet kapja, majd átadja az aktuális parancsmagnak a VirtualMachine08.</span><span class="sxs-lookup"><span data-stu-id="64447-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="64447-126">A parancs eltávolítja az SQL Server Virtual Machine bővítményt a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="64447-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="64447-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64447-127">PARAMETERS</span></span>

### <span data-ttu-id="64447-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="64447-128">-AutoBackupSettings</span></span>
<span data-ttu-id="64447-129">Az automatikus SQL Server biztonsági mentési beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="64447-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="64447-130">**AutoBackupSettings** -objektum létrehozásához használja az New-AzureVMSqlServerAutoBackupConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="64447-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="64447-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="64447-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="64447-132">Az automatikus SQL Server-javítás beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="64447-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="64447-133">**AutoPatchingSettings** -objektum létrehozásához használja az New-AzureVMSqlServerAutoPatchingConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="64447-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="64447-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64447-134">-DefaultProfile</span></span>
<span data-ttu-id="64447-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64447-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64447-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="64447-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="64447-137">-Hely</span><span class="sxs-lookup"><span data-stu-id="64447-137">-Location</span></span>
<span data-ttu-id="64447-138">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="64447-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="64447-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="64447-139">-Name</span></span>
<span data-ttu-id="64447-140">Annak az SQL Server-kiszolgálónak a nevét adja meg, amely a kiterjesztést adja.</span><span class="sxs-lookup"><span data-stu-id="64447-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="64447-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64447-141">-ResourceGroupName</span></span>
<span data-ttu-id="64447-142">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="64447-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="64447-143">-Verzió</span><span class="sxs-lookup"><span data-stu-id="64447-143">-Version</span></span>
<span data-ttu-id="64447-144">Az SQL Server-bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="64447-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="64447-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="64447-145">-VMName</span></span>
<span data-ttu-id="64447-146">Annak a virtuális gépnek a neve, amelyen a parancsmag az SQL Server-bővítményt állítja be.</span><span class="sxs-lookup"><span data-stu-id="64447-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="64447-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64447-147">CommonParameters</span></span>
<span data-ttu-id="64447-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64447-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64447-149">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64447-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64447-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64447-150">INPUTS</span></span>

### <span data-ttu-id="64447-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="64447-151">None</span></span>
<span data-ttu-id="64447-152">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="64447-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="64447-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64447-153">OUTPUTS</span></span>

### <span data-ttu-id="64447-154">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="64447-154">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="64447-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64447-155">NOTES</span></span>

## <span data-ttu-id="64447-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64447-156">RELATED LINKS</span></span>

[<span data-ttu-id="64447-157">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="64447-157">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="64447-158">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="64447-158">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="64447-159">Új – AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="64447-159">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="64447-160">Új – AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="64447-160">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="64447-161">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="64447-161">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="64447-162">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="64447-162">Update-AzVM</span></span>](./Update-AzVM.md)


