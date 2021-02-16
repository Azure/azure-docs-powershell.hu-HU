---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 1795216cbc18da2d503a1e0056d614337cd12785
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398240"
---
# <span data-ttu-id="bfd16-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="bfd16-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="bfd16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfd16-102">SYNOPSIS</span></span>
<span data-ttu-id="bfd16-103">Beállítja az Azure SQL Server-bővítményt egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="bfd16-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="bfd16-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bfd16-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfd16-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bfd16-105">DESCRIPTION</span></span>
<span data-ttu-id="bfd16-106">A **Set-AzVMSqlServerExtension** parancsmag beállítja az AzureSQL Server-bővítményt egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="bfd16-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="bfd16-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bfd16-107">EXAMPLES</span></span>

### <span data-ttu-id="bfd16-108">1. példa: Automatikus javítási beállítások megadása virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="bfd16-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="bfd16-109">Az első parancs a **New-AzureVMSqlServerAutoPatchingConfig** parancsmag használatával hoz létre konfigurációs objektumot.</span><span class="sxs-lookup"><span data-stu-id="bfd16-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="bfd16-110">A parancs a konfigurációt a $AutoPatchingConfig tárolja.</span><span class="sxs-lookup"><span data-stu-id="bfd16-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>

<span data-ttu-id="bfd16-111">A második parancs a VirtualMachine11 nevű virtuális gépet kapja meg a Service02 nevű szolgáltatásban a Get-AzVM parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="bfd16-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="bfd16-112">A parancs a folyamat műveleti operátorával átadja az objektumot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="bfd16-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="bfd16-113">Az aktuális parancsmag beállítja az automatikus javítási beállításokat $AutoPatchingConfig virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="bfd16-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="bfd16-114">A parancs átadja a virtuális gépet a Update-AzVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="bfd16-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="bfd16-115">2. példa: Automatikus biztonsági mentési beállítások megadása virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="bfd16-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="bfd16-116">Az első parancs a **New-AzureVMSqlServerAutoBackupConfig** parancsmag használatával hoz létre konfigurációs objektumot.</span><span class="sxs-lookup"><span data-stu-id="bfd16-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="bfd16-117">A parancs a konfigurációt a $AutoBackupConfig tárolja.</span><span class="sxs-lookup"><span data-stu-id="bfd16-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>

<span data-ttu-id="bfd16-118">A második parancs lekérte a VirtualMachine11 nevű virtuális gépet a Service02 nevű szolgáltatásban, majd átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="bfd16-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>

<span data-ttu-id="bfd16-119">Az aktuális parancsmag beállítja az automatikus biztonsági mentési beállításokat $AutoBackupConfig virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="bfd16-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="bfd16-120">A parancs átadja a virtuális gépet a Update-AzVM parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="bfd16-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="bfd16-121">3. példa: SQL Server-bővítmény letiltása virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="bfd16-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="bfd16-122">Ez a parancs egy VirtualMachine08 nevű virtuális gépet kap a Service03 szolgáltatásban, majd átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="bfd16-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="bfd16-123">A parancs letiltja az SQL Server virtuális gép bővítményét a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="bfd16-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="bfd16-124">4. példa: SQL Server-bővítmény eltávolítása egy adott virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="bfd16-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="bfd16-125">Ez a parancs egy VirtualMachine08 nevű virtuális gépet kap a Service03 szolgáltatásban, majd átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="bfd16-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="bfd16-126">A parancs eltávolítja az SQL Server virtuális gép bővítményét a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="bfd16-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="bfd16-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfd16-127">PARAMETERS</span></span>

### <span data-ttu-id="bfd16-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="bfd16-128">-AutoBackupSettings</span></span>
<span data-ttu-id="bfd16-129">Az SQL Server automatikus biztonsági mentési beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="bfd16-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="bfd16-130">Az **AutoBackupSettings objektum** létrehozásához használja a New-AzureVMSqlServerAutoBackupConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bfd16-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="bfd16-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="bfd16-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="bfd16-132">Az SQL Server automatikus javítási beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="bfd16-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="bfd16-133">**AutoPatchingSettings objektum** létrehozásához használja a New-AzureVMSqlServerAutoPatchingConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bfd16-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="bfd16-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfd16-134">-DefaultProfile</span></span>
<span data-ttu-id="bfd16-135">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bfd16-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfd16-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="bfd16-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="bfd16-137">-Location</span><span class="sxs-lookup"><span data-stu-id="bfd16-137">-Location</span></span>
<span data-ttu-id="bfd16-138">A virtuális gép helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="bfd16-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="bfd16-139">-Name</span><span class="sxs-lookup"><span data-stu-id="bfd16-139">-Name</span></span>
<span data-ttu-id="bfd16-140">Az SQL Server bővítmény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bfd16-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="bfd16-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfd16-141">-ResourceGroupName</span></span>
<span data-ttu-id="bfd16-142">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bfd16-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="bfd16-143">-Version</span><span class="sxs-lookup"><span data-stu-id="bfd16-143">-Version</span></span>
<span data-ttu-id="bfd16-144">Az SQL Server-bővítmény verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="bfd16-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="bfd16-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="bfd16-145">-VMName</span></span>
<span data-ttu-id="bfd16-146">Annak a virtuális gépnek a nevét adja meg, amelyen ez a parancsmag beállítja az SQL Server-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="bfd16-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="bfd16-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfd16-147">CommonParameters</span></span>
<span data-ttu-id="bfd16-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfd16-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfd16-149">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfd16-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfd16-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bfd16-150">INPUTS</span></span>

### <span data-ttu-id="bfd16-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="bfd16-151">None</span></span>
<span data-ttu-id="bfd16-152">Ez a parancsmag semmilyen bemenetet nem fogad el.</span><span class="sxs-lookup"><span data-stu-id="bfd16-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bfd16-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfd16-153">OUTPUTS</span></span>

### <span data-ttu-id="bfd16-154">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bfd16-154">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="bfd16-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bfd16-155">NOTES</span></span>

## <span data-ttu-id="bfd16-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bfd16-156">RELATED LINKS</span></span>

[<span data-ttu-id="bfd16-157">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="bfd16-157">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="bfd16-158">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="bfd16-158">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="bfd16-159">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="bfd16-159">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="bfd16-160">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="bfd16-160">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="bfd16-161">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="bfd16-161">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="bfd16-162">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="bfd16-162">Update-AzVM</span></span>](./Update-AzVM.md)


