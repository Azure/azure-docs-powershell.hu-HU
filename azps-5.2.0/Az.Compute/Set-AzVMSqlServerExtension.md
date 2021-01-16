---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 753c1de5b2f967ad321334231c77e379e11bc2ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334217"
---
# <span data-ttu-id="cd0f6-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="cd0f6-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="cd0f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd0f6-102">SYNOPSIS</span></span>
<span data-ttu-id="cd0f6-103">Beállítja az Azure SQL Server-bővítményt egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="cd0f6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cd0f6-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd0f6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cd0f6-105">DESCRIPTION</span></span>
<span data-ttu-id="cd0f6-106">A **Set-AzVMSqlServerExtension** parancsmag beállítja az AzureSQL Server-bővítményt egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="cd0f6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cd0f6-107">EXAMPLES</span></span>

### <span data-ttu-id="cd0f6-108">1. példa: Automatikus javítási beállítások megadása virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="cd0f6-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="cd0f6-109">Az első parancs a **New-AzVMSqlServerAutoPatchingConfig** parancsmag használatával hoz létre konfigurációs objektumot.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-109">The first command creates a configuration object by using the **New-AzVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="cd0f6-110">A parancs a konfigurációt a $AutoPatchingConfig tárolja.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>
<span data-ttu-id="cd0f6-111">A második parancs a VirtualMachine11 nevű virtuális gépet kapja meg a Service02 nevű szolgáltatásban a Get-AzVM parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="cd0f6-112">A parancs a folyamat műveleti operátorával átadja az objektumot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cd0f6-113">Az aktuális parancsmag beállítja az automatikus javítási beállításokat $AutoPatchingConfig virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="cd0f6-114">A parancs átadja a virtuális gépet a Update-AzVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="cd0f6-115">2. példa: Automatikus biztonsági mentési beállítások megadása virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="cd0f6-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="cd0f6-116">Az első parancs a **New-AzVMSqlServerAutoBackupConfig** parancsmag használatával hoz létre konfigurációs objektumot.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-116">The first command creates a configuration object by using the **New-AzVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="cd0f6-117">A parancs a konfigurációt a $AutoBackupConfig tárolja.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="cd0f6-118">A második parancs lejátssa a VirtualMachine11 nevű virtuális gépet a Service02 nevű szolgáltatásban, majd átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="cd0f6-119">Az aktuális parancsmag beállítja az automatikus biztonsági mentési beállításokat $AutoBackupConfig virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="cd0f6-120">A parancs átadja a virtuális gépet a Update-AzVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="cd0f6-121">3. példa: SQL Server-bővítmény letiltása virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="cd0f6-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="cd0f6-122">Ez a parancs egy VirtualMachine08 nevű virtuális gépet kap a Service03 szolgáltatásban, majd átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="cd0f6-123">A parancs letiltja az SQL Server virtuális gép bővítményét a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="cd0f6-124">4. példa: SQL Server-bővítmény eltávolítása egy adott virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="cd0f6-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="cd0f6-125">Ez a parancs egy VirtualMachine08 nevű virtuális gépet kap a Service03 szolgáltatásban, majd átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="cd0f6-126">A parancs eltávolítja az SQL Server virtuális gép bővítményét a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="cd0f6-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd0f6-127">PARAMETERS</span></span>

### <span data-ttu-id="cd0f6-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="cd0f6-128">-AutoBackupSettings</span></span>
<span data-ttu-id="cd0f6-129">Az SQL Server automatikus biztonsági mentési beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="cd0f6-130">Az **AutoBackupSettings objektum** létrehozásához használja a New-AzVMSqlServerAutoBackupConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-130">To create an **AutoBackupSettings** object , use the New-AzVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="cd0f6-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="cd0f6-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="cd0f6-132">Az SQL Server automatikus javítási beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="cd0f6-133">**AutoPatchingSettings objektum** létrehozásához használja a New-AzVMSqlServerAutoPatchingConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-133">To create an **AutoPatchingSettings** object , use the New-AzVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="cd0f6-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd0f6-134">-DefaultProfile</span></span>
<span data-ttu-id="cd0f6-135">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd0f6-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="cd0f6-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="cd0f6-137">-Location</span><span class="sxs-lookup"><span data-stu-id="cd0f6-137">-Location</span></span>
<span data-ttu-id="cd0f6-138">A virtuális gép helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="cd0f6-139">-Name</span><span class="sxs-lookup"><span data-stu-id="cd0f6-139">-Name</span></span>
<span data-ttu-id="cd0f6-140">Az SQL Server bővítmény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="cd0f6-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd0f6-141">-ResourceGroupName</span></span>
<span data-ttu-id="cd0f6-142">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="cd0f6-143">-Version</span><span class="sxs-lookup"><span data-stu-id="cd0f6-143">-Version</span></span>
<span data-ttu-id="cd0f6-144">Az SQL Server-bővítmény verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="cd0f6-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="cd0f6-145">-VMName</span></span>
<span data-ttu-id="cd0f6-146">Annak a virtuális gépnek a nevét adja meg, amelyen ez a parancsmag beállítja az SQL Server-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="cd0f6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd0f6-147">CommonParameters</span></span>
<span data-ttu-id="cd0f6-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd0f6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd0f6-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd0f6-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd0f6-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd0f6-150">INPUTS</span></span>

### <span data-ttu-id="cd0f6-151">System.String</span><span class="sxs-lookup"><span data-stu-id="cd0f6-151">System.String</span></span>

### <span data-ttu-id="cd0f6-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="cd0f6-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

### <span data-ttu-id="cd0f6-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="cd0f6-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

### <span data-ttu-id="cd0f6-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="cd0f6-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="cd0f6-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd0f6-155">OUTPUTS</span></span>

### <span data-ttu-id="cd0f6-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cd0f6-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="cd0f6-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cd0f6-157">NOTES</span></span>

## <span data-ttu-id="cd0f6-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd0f6-158">RELATED LINKS</span></span>

[<span data-ttu-id="cd0f6-159">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="cd0f6-159">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="cd0f6-160">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="cd0f6-160">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="cd0f6-161">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="cd0f6-161">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="cd0f6-162">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="cd0f6-162">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="cd0f6-163">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="cd0f6-163">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="cd0f6-164">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="cd0f6-164">Update-AzVM</span></span>](./Update-AzVM.md)


