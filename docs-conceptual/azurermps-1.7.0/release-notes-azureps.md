---
title: Az Azure PowerShell változásnaplója | Microsoft Docs
description: Az alábbiakban az Azure PowerShell legutóbbi kiadásában végrehajtott módosítások előzményei olvashatók.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 9f31fe404cca1162d5e4898287261f1bcbfa0f3a
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821853"
---
# <a name="release-notes"></a><span data-ttu-id="585f5-103">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="585f5-103">Release notes</span></span>

<span data-ttu-id="585f5-104">Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.</span><span class="sxs-lookup"><span data-stu-id="585f5-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-170"></a><span data-ttu-id="585f5-105">1.7.0-ás verzió</span><span class="sxs-lookup"><span data-stu-id="585f5-105">Version 1.7.0</span></span>

* <span data-ttu-id="585f5-106">**A -Force, –Confirm és $ConfirmPreference paraméterek viselkedésének módosítása minden parancsmag esetében. Ezt a megvalósítást azért módosítottuk, hogy megfeleljen a PowerShell irányelveinek. A legtöbb parancsmag esetében ez a Force paraméter eltávolítását, valamint a ShouldProcess adatkérés kihagyását jelenti. A felhasználóknak továbbá bele kell foglalniuk a következő paramétert a PowerShell-szkriptjeikbe: -Confirm:$false.**</span><span class="sxs-lookup"><span data-stu-id="585f5-106">**Behavioral change for -Force, –Confirm and $ConfirmPreference parameters for all cmdlets. We are changing this implementation to be in line with PowerShell guidelines. For most cmdlets, this means removing the Force parameter and to skip the ShouldProcess prompt, users will need to include the parameter: ‘-Confirm:$false’ in their PowerShell scripts.**</span></span> <span data-ttu-id="585f5-107">A módosítások a következő problémákat érintik:</span><span class="sxs-lookup"><span data-stu-id="585f5-107">This changes are addressing following issues:</span></span>
  - <span data-ttu-id="585f5-108">A –WhatIf funkció megvalósításának javítása, amely lehetővé teszi a felhasználók számára, hogy bármilyen tényleges módosítás nélkül megállapíthassák egy parancsmag vagy szkript hatásait</span><span class="sxs-lookup"><span data-stu-id="585f5-108">Correct implementation of –WhatIf functionality, allowing a user to determine the effects of a cmdlet or script without making any actual changes</span></span>
  - <span data-ttu-id="585f5-109">Az adatkérés vezérlése egy az egész munkamenetre kiterjedő $ConfirmPreference paraméter használatával, így a rendszer a végrehajtandó módosítás hatásai alapján szólítja fel a felhasználót (a parancsmag ConfirmImpact beállításában jelentett módon)</span><span class="sxs-lookup"><span data-stu-id="585f5-109">Control over prompting using a session-wide $ConfirmPreference, so that the user is prompted based on the impact of a prospective change (as reported in the ConfirmImpact setting in the cmdlet)</span></span>
  - <span data-ttu-id="585f5-110">A megerősítési felszólítások parancsmag-specifikus vezérlése a –Confirm paraméter használatával</span><span class="sxs-lookup"><span data-stu-id="585f5-110">Cmdlet-specific control over confirmation prompts using the –Confirm parameter</span></span>
  - <span data-ttu-id="585f5-111">A ShouldContinue és a –Force paraméterek konzisztens használata az összes parancsmagra vonatkozóan, valamint csak azon műveletek esetében, amelyekhez szükség van a felhasználó visszajelzésére a módosítások speciális jellege miatt (pl. rejtett fájlok törlése)</span><span class="sxs-lookup"><span data-stu-id="585f5-111">Consistent use of ShouldContinue and the –Force parameter across cmdlets, for only those actions that would require prompting from the user due to the special nature of the changes (for example, deleting hidden files)</span></span>
  - <span data-ttu-id="585f5-112">Konzisztencia más PowerShell-parancsmagokkal annak érdekében, hogy a PowerShell-szkriptek használatának más parancsmagokból származó ismerete azonnal alkalmazható legyen az Azure PowerShell-parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="585f5-112">Consistency with other PowerShell cmdlets, so that PowerShell scripting knowledge from other cmdlets is immediately applicable to the Azure PowerShell cmdlets.</span></span>

<span data-ttu-id="585f5-113">**Vegye figyelembe, hogy ha *minden esetben mellőzni szeretne minden adatkérést*, az Azure PowerShell-parancsmagok két paraméter megadását követelik meg:**</span><span class="sxs-lookup"><span data-stu-id="585f5-113">**Notice that now to *automatically skip all Prompts in all Circumstances* Azure PowerShell cmdlets require the user to supply two parameters:**</span></span>
```powershell
My-CmdletWithConfirmation –Confirm:$false -Force
```
* <span data-ttu-id="585f5-114">Azure Compute</span><span class="sxs-lookup"><span data-stu-id="585f5-114">Azure Compute</span></span>
  - <span data-ttu-id="585f5-115">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="585f5-115">Set-AzureRmVMADDomainExtension</span></span>
  - <span data-ttu-id="585f5-116">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="585f5-116">Get-AzureRmVMADDomainExtension</span></span>
  - <span data-ttu-id="585f5-117">-Redeploy paraméter a Restart-AzureVM parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="585f5-117">-Redeploy parameter for Restart-AzureVM</span></span>
  - <span data-ttu-id="585f5-118">-Validate paraméter a Move-AzureService, Move-AzureStorageAccount és Move-AzureVirtualNetwork parancsmagok esetében</span><span class="sxs-lookup"><span data-stu-id="585f5-118">-Validate parameter for Move-AzureService, Move-AzureStorageAccount, and Move-AzureVirtualNetwork</span></span>
  - <span data-ttu-id="585f5-119">A név- és verzióparaméterek továbbra is választhatók a bővítményparancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="585f5-119">Name and version parameters for extension cmdlets are optional as before.</span></span>
  - <span data-ttu-id="585f5-120">A New-AzureVM paraméter a virtuálisgép-objektumtól kaphatja meg a licenctípust.</span><span class="sxs-lookup"><span data-stu-id="585f5-120">New-AzureVM can get a license type from VM object.</span></span>
* <span data-ttu-id="585f5-121">Azure Storage</span><span class="sxs-lookup"><span data-stu-id="585f5-121">Azure Storage</span></span>
  - <span data-ttu-id="585f5-122">A Tags paraméter nevének módosítása a Tag névre, valamint a Tags paraméteralias hozzáadása</span><span class="sxs-lookup"><span data-stu-id="585f5-122">Change Tags Parameter to Tag, and add parameter alias Tags</span></span>
    + <span data-ttu-id="585f5-123">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="585f5-123">New-AzureRmStorageAccount</span></span>
    + <span data-ttu-id="585f5-124">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="585f5-124">Set-AzureRmStorageAccount</span></span>
* <span data-ttu-id="585f5-125">Azure Network-hálózat</span><span class="sxs-lookup"><span data-stu-id="585f5-125">Azure Network</span></span>
  - <span data-ttu-id="585f5-126">Új parancsmag hozzáadása a virtuális hálózatok közötti társviszony létesítéséhez</span><span class="sxs-lookup"><span data-stu-id="585f5-126">New cmdlet added for Virtual Network Peering</span></span>
* <span data-ttu-id="585f5-127">Azure Redis Cache</span><span class="sxs-lookup"><span data-stu-id="585f5-127">Azure Redis Cache</span></span>
  - <span data-ttu-id="585f5-128">Új parancsmag hozzáadása a Reset-AzureRmRedisCache parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="585f5-128">New cmdlet added for Reset-AzureRmRedisCache</span></span>
  - <span data-ttu-id="585f5-129">Új parancsmag hozzáadása a Export-AzureRmRedisCache parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="585f5-129">New cmdlet added for Export-AzureRmRedisCache</span></span>
  - <span data-ttu-id="585f5-130">Új parancsmag hozzáadása a Import-AzureRmRedisCache parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="585f5-130">New cmdlet added for Import-AzureRmRedisCache</span></span>
  - <span data-ttu-id="585f5-131">A New-AzureRmRedisCache parancsmag módosítása, hogy tartalmazza a vNet paramétermódosítását</span><span class="sxs-lookup"><span data-stu-id="585f5-131">Modified cmdlet New-AzureRmRedisCache to include parameter change for vNet</span></span>
* <span data-ttu-id="585f5-132">Azure SQL DB Backup/Restore</span><span class="sxs-lookup"><span data-stu-id="585f5-132">Azure SQL DB Backup/Restore</span></span>
  - <span data-ttu-id="585f5-133">Parancsmagok a hosszú távú adatmegőrzés céljából készített biztonsági mentésekhez</span><span class="sxs-lookup"><span data-stu-id="585f5-133">Cmdlets for LTR (Long Term Retention) backup feature</span></span>
  - <span data-ttu-id="585f5-134">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="585f5-134">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>
  - <span data-ttu-id="585f5-135">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="585f5-135">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>
  - <span data-ttu-id="585f5-136">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="585f5-136">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>
  - <span data-ttu-id="585f5-137">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="585f5-137">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>
  - <span data-ttu-id="585f5-138">A Restore-AzureRmSqlDatabase parancsmag mostantól támogatja a törölt adatbázisok időponthoz kötött visszaállítását</span><span class="sxs-lookup"><span data-stu-id="585f5-138">Restore-AzureRmSqlDatabase now supports point-in-time restore of a deleted database</span></span>
  - <span data-ttu-id="585f5-139">A Restore-AzureRmSqlDatabase mostantól támogatja a hosszú távú adatmegőrzés céljából készített biztonsági mentésekből történő helyreállítást</span><span class="sxs-lookup"><span data-stu-id="585f5-139">Restore-AzureRmSqlDatabase now supports restoring from a Long Term Retention backup</span></span>
* <span data-ttu-id="585f5-140">Azure LogicApp</span><span class="sxs-lookup"><span data-stu-id="585f5-140">Azure LogicApp</span></span>
  - <span data-ttu-id="585f5-141">LogicApp integrációs fiókok parancsmagjainak hozzáadása</span><span class="sxs-lookup"><span data-stu-id="585f5-141">Added LogicApp Integration accounts cmdlets.</span></span>
  - <span data-ttu-id="585f5-142">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="585f5-142">Get-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="585f5-143">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="585f5-143">Get-AzureRmIntegrationAccountCallbackUrl</span></span>
  - <span data-ttu-id="585f5-144">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="585f5-144">Get-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="585f5-145">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="585f5-145">Get-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="585f5-146">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="585f5-146">Get-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="585f5-147">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="585f5-147">Get-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="585f5-148">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="585f5-148">Get-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="585f5-149">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="585f5-149">New-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="585f5-150">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="585f5-150">New-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="585f5-151">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="585f5-151">New-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="585f5-152">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="585f5-152">New-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="585f5-153">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="585f5-153">New-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="585f5-154">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="585f5-154">New-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="585f5-155">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="585f5-155">Remove-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="585f5-156">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="585f5-156">Remove-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="585f5-157">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="585f5-157">Remove-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="585f5-158">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="585f5-158">Remove-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="585f5-159">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="585f5-159">Remove-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="585f5-160">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="585f5-160">Remove-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="585f5-161">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="585f5-161">Set-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="585f5-162">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="585f5-162">Set-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="585f5-163">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="585f5-163">Set-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="585f5-164">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="585f5-164">Set-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="585f5-165">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="585f5-165">Set-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="585f5-166">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="585f5-166">Set-AzureRmIntegrationAccountSchema</span></span>
* <span data-ttu-id="585f5-167">Azure Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="585f5-167">Azure Data Lake Store</span></span>
  - <span data-ttu-id="585f5-168">A fájl- és mappafeltöltések, illetve -letöltések teljesítményének jelentős mértékű javítása.</span><span class="sxs-lookup"><span data-stu-id="585f5-168">Drastically improve performance of file and folder upload and download.</span></span>
  - <span data-ttu-id="585f5-169">Ez magában foglalja a paraméternevek kismértékű módosítását a letöltések, valamint két új paraméter bevezetését a feltöltések esetében:</span><span class="sxs-lookup"><span data-stu-id="585f5-169">This includes a slight change to the parameter names for download and inclusion of two new parameters for upload:</span></span>
    + <span data-ttu-id="585f5-170">NumThreads -> PerFileThreadCount – Az egyetlen fájlban használandó szálak számát jelöli</span><span class="sxs-lookup"><span data-stu-id="585f5-170">NumThreads -> PerFileThreadCount, used to indicate the number of threads to use in a single file</span></span>
    + <span data-ttu-id="585f5-171">ConcurrentFileCount – A mappafeltöltés/-letöltés esetében a párhuzamosan feltölteni/letölteni kívánt fájlok számát jelöli.</span><span class="sxs-lookup"><span data-stu-id="585f5-171">ConcurrentFileCount, used to indicate the number of files to upload/download in parallel for folder upload/download.</span></span>
  - <span data-ttu-id="585f5-172">Az alapértelmezett szálkezelési értékek úgy lett kialakítva, hogy jobb általános teljesítményt biztosítsanak a legtöbb fájlméret esetében.</span><span class="sxs-lookup"><span data-stu-id="585f5-172">Default threading values are now designed to give a better all around throughput for most file sizes.</span></span> <span data-ttu-id="585f5-173">Ha a teljesítmény nem felel meg az elvárásnak, a fenti értékek az igényeknek megfelelően módosíthatók.</span><span class="sxs-lookup"><span data-stu-id="585f5-173">If performance is not as desired, the values above can be modified to meet requirements.</span></span>
* <span data-ttu-id="585f5-174">Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="585f5-174">Azure Data Lake Analytics</span></span>
  - <span data-ttu-id="585f5-175">A Get-AzureRMDataLakeAnalyticsDataSource parancsmag mostantól az összes adatforrást visszaadja, ha argumentumok nélkül hívják meg.</span><span class="sxs-lookup"><span data-stu-id="585f5-175">Get-AzureRMDataLakeAnalyticsDataSource now returns all data sources when called with no arguments.</span></span>
  - <span data-ttu-id="585f5-176">Ez a változtatás továbbá az adatforrás típusára vonatkozó paramétert is eltávolítja a parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="585f5-176">This change also removes the data source type parameter from the cmdlet.</span></span>
  - <span data-ttu-id="585f5-177">A változtatás eredményeképp a rendszer egy új objektumot ad vissza a listaművelet esetében, amely a következő tulajdonságokkal rendelkezik:</span><span class="sxs-lookup"><span data-stu-id="585f5-177">This change results in a new object being returned for the list operation with the following properties:</span></span>
    + <span data-ttu-id="585f5-178">Type – Az adatforrás típusa</span><span class="sxs-lookup"><span data-stu-id="585f5-178">Type, the type of data source</span></span>
    + <span data-ttu-id="585f5-179">Name – Az adatforrás neve</span><span class="sxs-lookup"><span data-stu-id="585f5-179">Name, the name of the data source</span></span>
    + <span data-ttu-id="585f5-180">IsDefault – Az értéke igaz, ha ez a fiók alapértelmezett adatforrása</span><span class="sxs-lookup"><span data-stu-id="585f5-180">IsDefault, set to true if this is the default data source for the account</span></span>
  - <span data-ttu-id="585f5-181">A Get-AzureRMDataLakeAnalyticsJob parancsmag javítása bizonyos dátum-/időeltolási értékek listázásakor, a submittedBefore és submittedAfter paraméterekre történő szűrés esetén.</span><span class="sxs-lookup"><span data-stu-id="585f5-181">Get-AzureRMDataLakeAnalyticsJob fixed for list for certain date time offset values when filtering on submittedBefore and submittedAfter.</span></span>
* <span data-ttu-id="585f5-182">Web Apps</span><span class="sxs-lookup"><span data-stu-id="585f5-182">Web Apps</span></span>
  - <span data-ttu-id="585f5-183">A Swap-AzureRmWebAppSlot parancsmag hozzáadása a normál felcserélés és a felcserélés előnézettel műveletek esetében</span><span class="sxs-lookup"><span data-stu-id="585f5-183">Add Swap-AzureRmWebAppSlot cmdlet for regular swap and swap with preview</span></span>
  - <span data-ttu-id="585f5-184">A Set-AzureRmWebAppSlot parancsmag kiterjesztése az automatikus felcserélés támogatásához</span><span class="sxs-lookup"><span data-stu-id="585f5-184">Extend Set-AzureRmWebAppSlot cmdlet to support auto swap</span></span>
* <span data-ttu-id="585f5-185">Azure API Management</span><span class="sxs-lookup"><span data-stu-id="585f5-185">Azure API Management</span></span>
  - <span data-ttu-id="585f5-186">Az Azure API Management telepítési parancsmagjainak javítása az AzureChinaCloud esetében.</span><span class="sxs-lookup"><span data-stu-id="585f5-186">Fixed Azure Api Management Deployment cmdlets for AzureChinaCloud.</span></span>
  - <span data-ttu-id="585f5-187">A Set-AzureRmApiManagementTenantGitAccess parancsmag eltávolítása, mivel a Git-hozzáférés alapértelmezés szerint engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="585f5-187">Removed cmdlet Set-AzureRmApiManagementTenantGitAccess as Git Access is enabled by Default.</span></span>
* <span data-ttu-id="585f5-188">Azure Recovery Services Backup</span><span class="sxs-lookup"><span data-stu-id="585f5-188">Azure Recovery Services Backup</span></span>
  - <span data-ttu-id="585f5-189">Az Azure SQL számítási feladatok támogatása</span><span class="sxs-lookup"><span data-stu-id="585f5-189">Added support for the Azure SQL workload</span></span>
  - <span data-ttu-id="585f5-190">A titkosított Azure virtuális gépek biztonsági mentésének és helyreállításának támogatása</span><span class="sxs-lookup"><span data-stu-id="585f5-190">Added support for backing up and restoring encrypted Azure VMs</span></span>
  - <span data-ttu-id="585f5-191">Backup-AzureRmRecoveryServicesBackupItem – Opcionális adatmegőrzési idő funkció hozzáadása a helyreállítási pontok esetében</span><span class="sxs-lookup"><span data-stu-id="585f5-191">Backup-AzureRmRecoveryServicesBackupItem - Added optional retention time feature for recovery points</span></span>
  - <span data-ttu-id="585f5-192">Kisebb, szűréssel kapcsolatos hibák javítása a Get-AzureRmRecoveryServicesBackupContainer és Get-AzureRmRecoveryServicesBackupItem parancsmagok esetében</span><span class="sxs-lookup"><span data-stu-id="585f5-192">Minor filter-related bug fixes in Get-AzureRmRecoveryServicesBackupContainer and Get-AzureRmRecoveryServicesBackupItem cmdlets</span></span>
* <span data-ttu-id="585f5-193">Azure Automation</span><span class="sxs-lookup"><span data-stu-id="585f5-193">Azure Automation</span></span>
  - <span data-ttu-id="585f5-194">A Get-AzureRmAutomationHybridWorkerGroup parancsmag hozzáadása</span><span class="sxs-lookup"><span data-stu-id="585f5-194">Added Get-AzureRmAutomationHybridWorkerGroup</span></span>
