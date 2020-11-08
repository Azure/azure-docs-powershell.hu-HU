---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 56C7B6F5-C2AC-4C5A-8930-645374694CC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 053bb1bfb31b90a91d69e50b77ac6411321014f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015790"
---
# <span data-ttu-id="cb60f-101">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="cb60f-101">Set-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="cb60f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb60f-102">SYNOPSIS</span></span>
<span data-ttu-id="cb60f-103">Egy virtuális gépen az Azure SQL Server-bővítményt állítja be.</span><span class="sxs-lookup"><span data-stu-id="cb60f-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="cb60f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb60f-104">SYNTAX</span></span>

### <span data-ttu-id="cb60f-105">EnableSqlServerExtension (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb60f-105">EnableSqlServerExtension (Default)</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>]
 [[-AutoPatchingSettings] <AutoPatchingSettings>] [[-AutoBackupSettings] <AutoBackupSettings>]
 [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cb60f-106">DisableSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="cb60f-106">DisableSqlServerExtension</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Disable] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb60f-107">UninstallSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="cb60f-107">UninstallSqlServerExtension</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Uninstall]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cb60f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb60f-108">DESCRIPTION</span></span>
<span data-ttu-id="cb60f-109">A **set-AzureVMSqlServerExtension** parancsmag egy virtuális gépen az Azure SQL Server-bővítményt állítja be.</span><span class="sxs-lookup"><span data-stu-id="cb60f-109">The **Set-AzureVMSqlServerExtension** cmdlet sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="cb60f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cb60f-110">EXAMPLES</span></span>

### <span data-ttu-id="cb60f-111">Példa 1: automatikus javítási beállítások megadása virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="cb60f-111">Example 1: Set auto-patching settings on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ServiceName" -Name "VMName" | Set-AzureVMSqlServerExtension -AutoPatchingSettings $APS | Update-AzureVM
```

<span data-ttu-id="cb60f-112">Ez a parancs beállítja az automatikus javítási beállításokat egy Azure virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="cb60f-112">This command sets auto-patching settings on an Azure virtual machine.</span></span>

### <span data-ttu-id="cb60f-113">2. példa: az automatikus biztonsági mentési beállítások beállítása virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="cb60f-113">Example 2: Set auto-backup settings on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ServiceName" -Name "VMName" | Set-AzureVMSqlServerExtension -AutoBackupSettings $ABS | Update-AzureVM
```

<span data-ttu-id="cb60f-114">Ez a parancs beállítja az automatikus biztonsági mentés beállításait az Azure Virtual Machine szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="cb60f-114">This command sets auto-backup settings on Azure virtual machine.</span></span>

### <span data-ttu-id="cb60f-115">3. példa: SQL Server-bővítmény letiltása virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="cb60f-115">Example 3: Disable an SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Set-AzureVMSqlServerExtension -Disable
```

<span data-ttu-id="cb60f-116">Ez a parancs letiltja az SQL Server Virtual Machine bővítményt egy adott virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="cb60f-116">This command disables SQL Server virtual machine extension on a given virtual machine.</span></span>

### <span data-ttu-id="cb60f-117">4. példa: egy SQL Server-bővítmény eltávolítása egy adott virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="cb60f-117">Example 4: Uninstall an SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Set-AzureVMSqlServerExtension -Uninstall
```

<span data-ttu-id="cb60f-118">Ez a parancs eltávolítja az SQL Server Virtual Machine bővítményt a VMName nevű virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="cb60f-118">This command uninstalls a SQL Server virtual machine extension on the virtual machine named VMName.</span></span>

## <span data-ttu-id="cb60f-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb60f-119">PARAMETERS</span></span>

### <span data-ttu-id="cb60f-120">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="cb60f-120">-AutoBackupSettings</span></span>
<span data-ttu-id="cb60f-121">Az automatikus SQL Server biztonsági mentési beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb60f-121">Specifies the automatic SQL Server backup settings.</span></span>

```yaml
Type: AutoBackupSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb60f-122">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="cb60f-122">-AutoPatchingSettings</span></span>
<span data-ttu-id="cb60f-123">Az automatikus SQL Server-javítás beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb60f-123">Specifies the automatic SQL Server patching settings.</span></span>

```yaml
Type: AutoPatchingSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb60f-124">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="cb60f-124">-Disable</span></span>
<span data-ttu-id="cb60f-125">Jelzi, hogy ez a parancsmag letiltja a bővítmény állapotát.</span><span class="sxs-lookup"><span data-stu-id="cb60f-125">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableSqlServerExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb60f-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="cb60f-126">-InformationAction</span></span>
<span data-ttu-id="cb60f-127">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="cb60f-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cb60f-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="cb60f-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cb60f-129">Folytassa</span><span class="sxs-lookup"><span data-stu-id="cb60f-129">Continue</span></span>
- <span data-ttu-id="cb60f-130">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="cb60f-130">Ignore</span></span>
- <span data-ttu-id="cb60f-131">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="cb60f-131">Inquire</span></span>
- <span data-ttu-id="cb60f-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cb60f-132">SilentlyContinue</span></span>
- <span data-ttu-id="cb60f-133">állj</span><span class="sxs-lookup"><span data-stu-id="cb60f-133">Stop</span></span>
- <span data-ttu-id="cb60f-134">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="cb60f-134">Suspend</span></span>

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

### <span data-ttu-id="cb60f-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cb60f-135">-InformationVariable</span></span>
<span data-ttu-id="cb60f-136">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="cb60f-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cb60f-137">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="cb60f-137">-KeyVaultCredentialSettings</span></span>
<span data-ttu-id="cb60f-138">Adja meg a kulcsfájl hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="cb60f-138">Specifies key vault credential settings.</span></span>

```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb60f-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="cb60f-139">-Profile</span></span>
<span data-ttu-id="cb60f-140">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="cb60f-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cb60f-141">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="cb60f-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cb60f-142">-Hivatkozásnév</span><span class="sxs-lookup"><span data-stu-id="cb60f-142">-ReferenceName</span></span>
<span data-ttu-id="cb60f-143">Az SQL Server-bővítmény hivatkozási nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb60f-143">Specifies the reference name of the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb60f-144">-Uninstall</span><span class="sxs-lookup"><span data-stu-id="cb60f-144">-Uninstall</span></span>
<span data-ttu-id="cb60f-145">Azt jelzi, hogy ez a parancsmag eltávolítja az SQL Server-bővítményt a virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="cb60f-145">Indicates that this cmdlet uninstalls the SQL Server extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallSqlServerExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb60f-146">-Verzió</span><span class="sxs-lookup"><span data-stu-id="cb60f-146">-Version</span></span>
<span data-ttu-id="cb60f-147">Annak az SQL Server-bővítménynek a verziószámát adja meg, amely Get-AzureVMSqlServerExtension lekéri a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="cb60f-147">Specifies the version of the SQL Server extension that Get-AzureVMSqlServerExtension retrieves settings from.</span></span>

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

### <span data-ttu-id="cb60f-148">-VM</span><span class="sxs-lookup"><span data-stu-id="cb60f-148">-VM</span></span>
<span data-ttu-id="cb60f-149">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb60f-149">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="cb60f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb60f-150">CommonParameters</span></span>
<span data-ttu-id="cb60f-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb60f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb60f-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb60f-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb60f-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb60f-153">INPUTS</span></span>

## <span data-ttu-id="cb60f-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb60f-154">OUTPUTS</span></span>

## <span data-ttu-id="cb60f-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb60f-155">NOTES</span></span>

## <span data-ttu-id="cb60f-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb60f-156">RELATED LINKS</span></span>

[<span data-ttu-id="cb60f-157">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="cb60f-157">Get-AzureVMSqlServerExtension</span></span>](./Get-AzureVMSqlServerExtension.md)

[<span data-ttu-id="cb60f-158">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="cb60f-158">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)


