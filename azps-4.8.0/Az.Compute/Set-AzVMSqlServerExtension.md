---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 753c1de5b2f967ad321334231c77e379e11bc2ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024100"
---
# <span data-ttu-id="27eac-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="27eac-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="27eac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27eac-102">SYNOPSIS</span></span>
<span data-ttu-id="27eac-103">Egy virtuális gépen az Azure SQL Server-bővítményt állítja be.</span><span class="sxs-lookup"><span data-stu-id="27eac-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="27eac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27eac-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27eac-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="27eac-105">DESCRIPTION</span></span>
<span data-ttu-id="27eac-106">A **set-AzVMSqlServerExtension** parancsmag egy virtuális gépen beállítja a AzureSQL Server bővítményt.</span><span class="sxs-lookup"><span data-stu-id="27eac-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="27eac-107">Példák</span><span class="sxs-lookup"><span data-stu-id="27eac-107">EXAMPLES</span></span>

### <span data-ttu-id="27eac-108">1. példa: automatikus javítási beállítások megadása virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="27eac-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="27eac-109">Az első parancs a **New-AzVMSqlServerAutoPatchingConfig** parancsmag segítségével hoz létre konfigurációs objektumot.</span><span class="sxs-lookup"><span data-stu-id="27eac-109">The first command creates a configuration object by using the **New-AzVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="27eac-110">A parancs a $AutoPatchingConfig változóban tárolja a konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="27eac-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>
<span data-ttu-id="27eac-111">A második parancs a VirtualMachine11 nevű virtuális gépet a Service02 nevű szolgáltatáson keresztül kapja meg az Get-AzVM parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="27eac-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="27eac-112">A parancs a csővezeték-kezelő használatával továbbítja az objektumot az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="27eac-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="27eac-113">Az aktuális parancsmag a virtuális gép $AutoPatchingConfig automatikus javítási beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="27eac-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="27eac-114">A parancs átadja a virtuális gépet az Update-AzVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="27eac-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="27eac-115">2. példa: automatikus biztonsági mentési beállítások megadása virtuális számítógépen</span><span class="sxs-lookup"><span data-stu-id="27eac-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="27eac-116">Az első parancs a **New-AzVMSqlServerAutoBackupConfig** parancsmag segítségével hoz létre konfigurációs objektumot.</span><span class="sxs-lookup"><span data-stu-id="27eac-116">The first command creates a configuration object by using the **New-AzVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="27eac-117">A parancs a $AutoBackupConfig változóban tárolja a konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="27eac-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="27eac-118">A második parancs megkapja a VirtualMachine11 nevű virtuális gépet a Service02 nevű szolgáltatásban, majd átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="27eac-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="27eac-119">A jelenlegi parancsmag a virtuális gép $AutoBackupConfigban található automatikus biztonsági mentési beállításokat állítja be.</span><span class="sxs-lookup"><span data-stu-id="27eac-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="27eac-120">A parancs átadja a virtuális gépet az Update-AzVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="27eac-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="27eac-121">3. példa: SQL Server-bővítmény letiltása virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="27eac-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="27eac-122">Ez a parancs a Service03 nevű virtuális gépet kapja, majd átadja az aktuális parancsmagnak a VirtualMachine08.</span><span class="sxs-lookup"><span data-stu-id="27eac-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="27eac-123">A parancs letiltja az SQL Server Virtual Machine bővítményt a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="27eac-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="27eac-124">4. példa: az SQL Server-bővítmények eltávolítása egy adott virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="27eac-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="27eac-125">Ez a parancs a Service03 nevű virtuális gépet kapja, majd átadja az aktuális parancsmagnak a VirtualMachine08.</span><span class="sxs-lookup"><span data-stu-id="27eac-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="27eac-126">A parancs eltávolítja az SQL Server Virtual Machine bővítményt a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="27eac-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="27eac-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27eac-127">PARAMETERS</span></span>

### <span data-ttu-id="27eac-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="27eac-128">-AutoBackupSettings</span></span>
<span data-ttu-id="27eac-129">Az automatikus SQL Server biztonsági mentési beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="27eac-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="27eac-130">**AutoBackupSettings** -objektum létrehozásához használja az New-AzVMSqlServerAutoBackupConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="27eac-130">To create an **AutoBackupSettings** object , use the New-AzVMSqlServerAutoBackupConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoBackupSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27eac-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="27eac-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="27eac-132">Az automatikus SQL Server-javítás beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="27eac-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="27eac-133">**AutoPatchingSettings** -objektum létrehozásához használja az New-AzVMSqlServerAutoPatchingConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="27eac-133">To create an **AutoPatchingSettings** object , use the New-AzVMSqlServerAutoPatchingConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoPatchingSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27eac-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27eac-134">-DefaultProfile</span></span>
<span data-ttu-id="27eac-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27eac-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27eac-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="27eac-136">-KeyVaultCredentialSettings</span></span>
```yaml
Type: Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27eac-137">-Hely</span><span class="sxs-lookup"><span data-stu-id="27eac-137">-Location</span></span>
<span data-ttu-id="27eac-138">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="27eac-138">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27eac-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="27eac-139">-Name</span></span>
<span data-ttu-id="27eac-140">Annak az SQL Server-kiszolgálónak a nevét adja meg, amely a kiterjesztést adja.</span><span class="sxs-lookup"><span data-stu-id="27eac-140">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27eac-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27eac-141">-ResourceGroupName</span></span>
<span data-ttu-id="27eac-142">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="27eac-142">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27eac-143">-Verzió</span><span class="sxs-lookup"><span data-stu-id="27eac-143">-Version</span></span>
<span data-ttu-id="27eac-144">Az SQL Server-bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="27eac-144">Specifies the version of the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27eac-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="27eac-145">-VMName</span></span>
<span data-ttu-id="27eac-146">Annak a virtuális gépnek a neve, amelyen a parancsmag az SQL Server-bővítményt állítja be.</span><span class="sxs-lookup"><span data-stu-id="27eac-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27eac-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27eac-147">CommonParameters</span></span>
<span data-ttu-id="27eac-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27eac-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27eac-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="27eac-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27eac-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27eac-150">INPUTS</span></span>

### <span data-ttu-id="27eac-151">System. String</span><span class="sxs-lookup"><span data-stu-id="27eac-151">System.String</span></span>

### <span data-ttu-id="27eac-152">Microsoft. Azure. commands. kiszámítás. AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="27eac-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

### <span data-ttu-id="27eac-153">Microsoft. Azure. commands. kiszámítás. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="27eac-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

### <span data-ttu-id="27eac-154">Microsoft. Azure. commands. kiszámítás. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="27eac-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="27eac-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27eac-155">OUTPUTS</span></span>

### <span data-ttu-id="27eac-156">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="27eac-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="27eac-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27eac-157">NOTES</span></span>

## <span data-ttu-id="27eac-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27eac-158">RELATED LINKS</span></span>

[<span data-ttu-id="27eac-159">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="27eac-159">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="27eac-160">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="27eac-160">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="27eac-161">Új – AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="27eac-161">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="27eac-162">Új – AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="27eac-162">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="27eac-163">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="27eac-163">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="27eac-164">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="27eac-164">Update-AzVM</span></span>](./Update-AzVM.md)


