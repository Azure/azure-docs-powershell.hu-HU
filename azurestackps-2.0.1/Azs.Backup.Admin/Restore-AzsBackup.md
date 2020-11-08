---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/restore-azsbackup
schema: 2.0.0
ms.openlocfilehash: d441c74817ccaf1b32b7caf6fe811f6a5a4789da
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015353"
---
# <span data-ttu-id="e2874-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="e2874-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="e2874-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2874-102">SYNOPSIS</span></span>
<span data-ttu-id="e2874-103">Biztonsági másolat visszaállítása</span><span class="sxs-lookup"><span data-stu-id="e2874-103">Restore a backup.</span></span>

## <span data-ttu-id="e2874-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2874-104">SYNTAX</span></span>

### <span data-ttu-id="e2874-105">RestoreExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e2874-105">RestoreExpanded (Default)</span></span>
```
Restore-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DecryptionCertPassword <SecureString>] [-DecryptionCertPath <String>] [-RoleName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e2874-106">Visszaállítása</span><span class="sxs-lookup"><span data-stu-id="e2874-106">Restore</span></span>
```
Restore-AzsBackup -Name <String> -RestoreOption <IRestoreOptions> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e2874-107">RestoreViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e2874-107">RestoreViaIdentity</span></span>
```
Restore-AzsBackup -InputObject <IBackupAdminIdentity> -RestoreOption <IRestoreOptions>
 [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e2874-108">RestoreViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e2874-108">RestoreViaIdentityExpanded</span></span>
```
Restore-AzsBackup -InputObject <IBackupAdminIdentity> [-DecryptionCertPassword <SecureString>]
 [-DecryptionCertPath <String>] [-RoleName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e2874-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2874-109">DESCRIPTION</span></span>
<span data-ttu-id="e2874-110">Biztonsági másolat visszaállítása</span><span class="sxs-lookup"><span data-stu-id="e2874-110">Restore a backup.</span></span>

## <span data-ttu-id="e2874-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e2874-111">EXAMPLES</span></span>

### <span data-ttu-id="e2874-112">1. példa: biztonsági másolat visszaállítása</span><span class="sxs-lookup"><span data-stu-id="e2874-112">Example 1: Restore Backup</span></span>
```powershell
PS C:\> Restore-AzsBackup -Name $backupResourceName -DecryptionCertPath $decryptionCertPath -DecryptionCertPassword $decryptionCertPassword

```

<span data-ttu-id="e2874-113">Visszaállíthatja az Azure-halom biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="e2874-113">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="e2874-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2874-114">PARAMETERS</span></span>

### <span data-ttu-id="e2874-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2874-115">-AsJob</span></span>
<span data-ttu-id="e2874-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="e2874-116">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e2874-117">-DecryptionCertPassword</span><span class="sxs-lookup"><span data-stu-id="e2874-117">-DecryptionCertPassword</span></span>
<span data-ttu-id="e2874-118">A visszafejtési tanúsítvány jelszava.</span><span class="sxs-lookup"><span data-stu-id="e2874-118">The password for the decryption certificate.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e2874-119">-DecryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="e2874-119">-DecryptionCertPath</span></span>
<span data-ttu-id="e2874-120">A visszafejtési tanúsítvány fájljának elérési útja titkos kulccsal (. pfx)</span><span class="sxs-lookup"><span data-stu-id="e2874-120">Path to the decryption cert file with private key (.pfx).</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e2874-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2874-121">-DefaultProfile</span></span>
<span data-ttu-id="e2874-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2874-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e2874-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e2874-123">-Force</span></span>
<span data-ttu-id="e2874-124">Nem kér megerősítést</span><span class="sxs-lookup"><span data-stu-id="e2874-124">Don't ask for confirmation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e2874-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2874-125">-InputObject</span></span>
<span data-ttu-id="e2874-126">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e2874-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: RestoreViaIdentity, RestoreViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e2874-127">-Hely</span><span class="sxs-lookup"><span data-stu-id="e2874-127">-Location</span></span>
<span data-ttu-id="e2874-128">A biztonsági másolat helyének neve.</span><span class="sxs-lookup"><span data-stu-id="e2874-128">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e2874-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e2874-129">-Name</span></span>
<span data-ttu-id="e2874-130">A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="e2874-130">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e2874-131">-Várva</span><span class="sxs-lookup"><span data-stu-id="e2874-131">-NoWait</span></span>
<span data-ttu-id="e2874-132">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="e2874-132">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e2874-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2874-133">-PassThru</span></span>
<span data-ttu-id="e2874-134">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="e2874-134">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e2874-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2874-135">-ResourceGroupName</span></span>
<span data-ttu-id="e2874-136">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e2874-136">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e2874-137">-RestoreOption</span><span class="sxs-lookup"><span data-stu-id="e2874-137">-RestoreOption</span></span>
<span data-ttu-id="e2874-138">A visszaállítási beállítások tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="e2874-138">Properties for restore options.</span></span>
<span data-ttu-id="e2874-139">A kivitelezéshez tekintse meg a RESTOREOPTION tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="e2874-139">To construct, see NOTES section for RESTOREOPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IRestoreOptions
Parameter Sets: Restore, RestoreViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e2874-140">-RoleName</span><span class="sxs-lookup"><span data-stu-id="e2874-140">-RoleName</span></span>
<span data-ttu-id="e2874-141">Az Azure-köteg szerepkör neve a visszaállításhoz, az összes infrastruktúra-szerepkör esetén az üres értékre van állítva</span><span class="sxs-lookup"><span data-stu-id="e2874-141">The Azure Stack role name for restore, set it to empty for all infrastructure role</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e2874-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2874-142">-SubscriptionId</span></span>
<span data-ttu-id="e2874-143">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="e2874-143">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e2874-144">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e2874-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e2874-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e2874-145">-Confirm</span></span>
<span data-ttu-id="e2874-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e2874-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e2874-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2874-147">-WhatIf</span></span>
<span data-ttu-id="e2874-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e2874-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2874-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e2874-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e2874-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2874-150">CommonParameters</span></span>
<span data-ttu-id="e2874-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2874-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2874-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e2874-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2874-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2874-153">INPUTS</span></span>

### <span data-ttu-id="e2874-154">Microsoft. Azure. PowerShell. parancsmagok. BackupAdmin. models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e2874-154">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="e2874-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2874-155">OUTPUTS</span></span>

### <span data-ttu-id="e2874-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2874-156">System.Boolean</span></span>



## <span data-ttu-id="e2874-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2874-157">NOTES</span></span>

<span data-ttu-id="e2874-158">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="e2874-158">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e2874-159">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="e2874-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e2874-160">INPUTOBJECT <IBackupAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="e2874-160">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e2874-161">`[Backup <String>]`: A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="e2874-161">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="e2874-162">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e2874-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e2874-163">`[Location <String>]`: A biztonsági másolat helyének neve.</span><span class="sxs-lookup"><span data-stu-id="e2874-163">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="e2874-164">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e2874-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="e2874-165">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="e2874-165">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e2874-166">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e2874-166">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="e2874-167">RESTOREOPTION <IRestoreOptions> : a visszaállítási beállítások tulajdonságai.</span><span class="sxs-lookup"><span data-stu-id="e2874-167">RESTOREOPTION <IRestoreOptions>: Properties for restore options.</span></span>
  - <span data-ttu-id="e2874-168">`[DecryptionCertBase64 <String>]`: A tanúsítvány-fájl nyers adatainak Base64-karakterláncban való megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="e2874-168">`[DecryptionCertBase64 <String>]`: The certificate file raw data in Base64 string.</span></span> <span data-ttu-id="e2874-169">Ennek a személyes kulccsal. pfx fájlnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="e2874-169">This should be the .pfx file with the private key.</span></span>
  - <span data-ttu-id="e2874-170">`[DecryptionCertPassword <String>]`: A visszafejtési tanúsítvány jelszava.</span><span class="sxs-lookup"><span data-stu-id="e2874-170">`[DecryptionCertPassword <String>]`: The password for the decryption certificate.</span></span>
  - <span data-ttu-id="e2874-171">`[RoleName <String>]`: Az Azure-köteg szerepkör neve a visszaállításhoz, az összes infrastrukturális szerepkör esetén üresre állítható</span><span class="sxs-lookup"><span data-stu-id="e2874-171">`[RoleName <String>]`: The Azure Stack role name for restore, set it to empty for all infrastructure role</span></span>

## <span data-ttu-id="e2874-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2874-172">RELATED LINKS</span></span>

