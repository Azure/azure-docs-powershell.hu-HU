---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/update-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Update-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Update-AzADDomainService.md
ms.openlocfilehash: 7acebe247009c95f9d504dc09b2729eeb5aabbbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143818"
---
# <span data-ttu-id="ef62b-101">Update-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="ef62b-101">Update-AzADDomainService</span></span>

## <span data-ttu-id="ef62b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef62b-102">SYNOPSIS</span></span>
<span data-ttu-id="ef62b-103">A tartományszolgáltatás frissítése művelettel frissítheti a meglévő telepítést.</span><span class="sxs-lookup"><span data-stu-id="ef62b-103">The Update Domain Service operation can be used to update the existing deployment.</span></span>
<span data-ttu-id="ef62b-104">A frissítési hívás csak a JAVÍTÁS törzsében felsorolt tulajdonságokat támogatja.</span><span class="sxs-lookup"><span data-stu-id="ef62b-104">The update call only supports the properties listed in the PATCH body.</span></span>

## <span data-ttu-id="ef62b-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ef62b-105">SYNTAX</span></span>

### <span data-ttu-id="ef62b-106">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef62b-106">UpdateExpanded (Default)</span></span>
```
Update-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DomainConfigurationType <String>] [-DomainSecuritySettingNtlmV1 <String>]
 [-DomainSecuritySettingSyncKerberosPassword <String>] [-DomainSecuritySettingSyncNtlmPassword <String>]
 [-DomainSecuritySettingSyncOnPremPassword <String>] [-DomainSecuritySettingTlsV1 <String>]
 [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>] [-LdapSettingExternalAccess <String>]
 [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ReplicaSet <IReplicaSet[]>] [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ef62b-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ef62b-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DomainConfigurationType <String>]
 [-DomainSecuritySettingNtlmV1 <String>] [-DomainSecuritySettingSyncKerberosPassword <String>]
 [-DomainSecuritySettingSyncNtlmPassword <String>] [-DomainSecuritySettingSyncOnPremPassword <String>]
 [-DomainSecuritySettingTlsV1 <String>] [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>]
 [-LdapSettingExternalAccess <String>] [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ReplicaSet <IReplicaSet[]>] [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ef62b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ef62b-108">DESCRIPTION</span></span>
<span data-ttu-id="ef62b-109">A tartományszolgáltatás frissítése művelettel frissítheti a meglévő telepítést.</span><span class="sxs-lookup"><span data-stu-id="ef62b-109">The Update Domain Service operation can be used to update the existing deployment.</span></span>
<span data-ttu-id="ef62b-110">A frissítési hívás csak a JAVÍTÁS törzsében felsorolt tulajdonságokat támogatja.</span><span class="sxs-lookup"><span data-stu-id="ef62b-110">The update call only supports the properties listed in the PATCH body.</span></span>

## <span data-ttu-id="ef62b-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ef62b-111">EXAMPLES</span></span>

### <span data-ttu-id="ef62b-112">1. példa: AzADDomainService frissítése ResourceGroupName és Név szerint</span><span class="sxs-lookup"><span data-stu-id="ef62b-112">Example 1: Update AzADDomainService By ResourceGroupName and Name</span></span>
```powershell
PS C:\> $ADDomainSetting = New-AzADDomainServiceDomainSecuritySettingObject -TlsV1 Disabled
Update-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain -DomainSecuritySetting $ADDomainSetting

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="ef62b-113">Update AzADDomainService By ResourceGroupName and Name</span><span class="sxs-lookup"><span data-stu-id="ef62b-113">Update AzADDomainService By ResourceGroupName and Name</span></span>

### <span data-ttu-id="ef62b-114">2. példa: AzADDomainService frissítése Inputobject szerint</span><span class="sxs-lookup"><span data-stu-id="ef62b-114">Example 2: Update AzADDomainService By Inputobject</span></span>
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
$ADDomainSetting = New-AzADDomainServiceDomainSecuritySettingObject -TlsV1 Disabled
Update-AzADDomainService -InputObject $getAzAddomain -DomainSecuritySetting $ADDomainSetting

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="ef62b-115">AzADDomainService frissítése Inputobject szerint</span><span class="sxs-lookup"><span data-stu-id="ef62b-115">Update AzADDomainService By Inputobject</span></span>

## <span data-ttu-id="ef62b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef62b-116">PARAMETERS</span></span>

### <span data-ttu-id="ef62b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef62b-117">-AsJob</span></span>
<span data-ttu-id="ef62b-118">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="ef62b-118">Run the command as a job</span></span>

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

### <span data-ttu-id="ef62b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef62b-119">-DefaultProfile</span></span>
<span data-ttu-id="ef62b-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef62b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef62b-121">-DomainConfigurationType</span><span class="sxs-lookup"><span data-stu-id="ef62b-121">-DomainConfigurationType</span></span>
<span data-ttu-id="ef62b-122">Tartománykonfigurációs típus</span><span class="sxs-lookup"><span data-stu-id="ef62b-122">Domain Configuration Type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-123">-DomainSecuritySettingNtlmV1</span><span class="sxs-lookup"><span data-stu-id="ef62b-123">-DomainSecuritySettingNtlmV1</span></span>
<span data-ttu-id="ef62b-124">Jelölő annak megállapításához, hogy az NtlmV1 engedélyezve van-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="ef62b-124">A flag to determine whether or not NtlmV1 is enabled or disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-125">-DomainSecuritySettingSyncKerberosPassword</span><span class="sxs-lookup"><span data-stu-id="ef62b-125">-DomainSecuritySettingSyncKerberosPassword</span></span>
<span data-ttu-id="ef62b-126">Jelölő annak megállapításához, hogy a SyncKerberosPasswords engedélyezve van-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="ef62b-126">A flag to determine whether or not SyncKerberosPasswords is enabled or disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-127">-DomainSecuritySettingSyncNtlmPassword</span><span class="sxs-lookup"><span data-stu-id="ef62b-127">-DomainSecuritySettingSyncNtlmPassword</span></span>
<span data-ttu-id="ef62b-128">Jelölő annak megállapításához, hogy a SyncNtlmPasswords engedélyezve van-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="ef62b-128">A flag to determine whether or not SyncNtlmPasswords is enabled or disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-129">-DomainSecuritySettingSyncOnPremPassword</span><span class="sxs-lookup"><span data-stu-id="ef62b-129">-DomainSecuritySettingSyncOnPremPassword</span></span>
<span data-ttu-id="ef62b-130">Jelölő annak megállapításához, hogy a SyncOnPremPasswords engedélyezve van-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="ef62b-130">A flag to determine whether or not SyncOnPremPasswords is enabled or disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-131">-DomainSecuritySettingTlsV1</span><span class="sxs-lookup"><span data-stu-id="ef62b-131">-DomainSecuritySettingTlsV1</span></span>
<span data-ttu-id="ef62b-132">Jelölő annak megállapításához, hogy a TlsV1 engedélyezve van-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="ef62b-132">A flag to determine whether or not TlsV1 is enabled or disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-133">-FilteredSync</span><span class="sxs-lookup"><span data-stu-id="ef62b-133">-FilteredSync</span></span>
<span data-ttu-id="ef62b-134">A csoportalapú szűrt szinkronizálás bekapcsolásának engedélyezése vagy letiltás jelölője</span><span class="sxs-lookup"><span data-stu-id="ef62b-134">Enabled or Disabled flag to turn on Group-based filtered sync</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-135">-ForestTrust</span><span class="sxs-lookup"><span data-stu-id="ef62b-135">-ForestTrust</span></span>
<span data-ttu-id="ef62b-136">A felépíteni szükséges erőforrás-erdő beállításainak listája a MEGJEGYZÉSEK szakaszban található a FORESTTRUST tulajdonságokhoz, és hozzon létre egy kivonattáblát.</span><span class="sxs-lookup"><span data-stu-id="ef62b-136">List of settings for Resource Forest To construct, see NOTES section for FORESTTRUST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IForestTrust[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef62b-137">-InputObject</span></span>
<span data-ttu-id="ef62b-138">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ef62b-138">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-139">-LdapSettingExternalAccess</span><span class="sxs-lookup"><span data-stu-id="ef62b-139">-LdapSettingExternalAccess</span></span>
<span data-ttu-id="ef62b-140">Jelölő annak megállapításához, hogy engedélyezve vagy letiltva van-e az LDAP-hozzáférés biztonságos interneten keresztül.</span><span class="sxs-lookup"><span data-stu-id="ef62b-140">A flag to determine whether or not Secure LDAP access over the internet is enabled or disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-141">-LdapSettingLdaps</span><span class="sxs-lookup"><span data-stu-id="ef62b-141">-LdapSettingLdaps</span></span>
<span data-ttu-id="ef62b-142">Jelölő annak megállapításához, hogy a Biztonságos LDAP engedélyezve van-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="ef62b-142">A flag to determine whether or not Secure LDAP is enabled or disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-143">-LdapSettingPfxCertificate</span><span class="sxs-lookup"><span data-stu-id="ef62b-143">-LdapSettingPfxCertificate</span></span>
<span data-ttu-id="ef62b-144">A Biztonságos LDAP konfigurálhoz szükséges tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="ef62b-144">The certificate required to configure Secure LDAP.</span></span>
<span data-ttu-id="ef62b-145">Az itt átadott paraméternek a pfx-fájl base64encoded típusú reprezentációja kell, hogy legyen.</span><span class="sxs-lookup"><span data-stu-id="ef62b-145">The parameter passed here should be a base64encoded representation of the certificate pfx file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-146">-LdapSettingPfxCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="ef62b-146">-LdapSettingPfxCertificatePassword</span></span>
<span data-ttu-id="ef62b-147">A megadott Secure LDAP-tanúsítvány pfx fájljának visszafejtéséhez szükséges jelszó.</span><span class="sxs-lookup"><span data-stu-id="ef62b-147">The password to decrypt the provided Secure LDAP certificate pfx file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-148">-Name</span><span class="sxs-lookup"><span data-stu-id="ef62b-148">-Name</span></span>
<span data-ttu-id="ef62b-149">A tartományszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="ef62b-149">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-150">-NotificationSettingAdditionalRecipient</span><span class="sxs-lookup"><span data-stu-id="ef62b-150">-NotificationSettingAdditionalRecipient</span></span>
<span data-ttu-id="ef62b-151">A további címzettek listája</span><span class="sxs-lookup"><span data-stu-id="ef62b-151">The list of additional recipients</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-152">-NotificationSettingNotifyDcAdmin</span><span class="sxs-lookup"><span data-stu-id="ef62b-152">-NotificationSettingNotifyDcAdmin</span></span>
<span data-ttu-id="ef62b-153">Tartományvezérlő-rendszergazdák értesítése</span><span class="sxs-lookup"><span data-stu-id="ef62b-153">Should domain controller admins be notified</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-154">-NotificationSettingNotifyGlobalAdmin</span><span class="sxs-lookup"><span data-stu-id="ef62b-154">-NotificationSettingNotifyGlobalAdmin</span></span>
<span data-ttu-id="ef62b-155">A globális rendszergazdák értesítése</span><span class="sxs-lookup"><span data-stu-id="ef62b-155">Should global admins be notified</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-156">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ef62b-156">-NoWait</span></span>
<span data-ttu-id="ef62b-157">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="ef62b-157">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ef62b-158">-ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="ef62b-158">-ReplicaSet</span></span>
<span data-ttu-id="ef62b-159">A létrehozni szükséges replikakészletek listája a NOTES (JEGYZETEK) című szakaszban található a REPLIKAKÉSZLET tulajdonságaihoz, és létrehozhat egy kivonattáblát.</span><span class="sxs-lookup"><span data-stu-id="ef62b-159">List of ReplicaSets To construct, see NOTES section for REPLICASET properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IReplicaSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-160">-ResourceForest</span><span class="sxs-lookup"><span data-stu-id="ef62b-160">-ResourceForest</span></span>
<span data-ttu-id="ef62b-161">Erőforrás-erdő</span><span class="sxs-lookup"><span data-stu-id="ef62b-161">Resource Forest</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef62b-162">-ResourceGroupName</span></span>
<span data-ttu-id="ef62b-163">A felhasználó előfizetésében található erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ef62b-163">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="ef62b-164">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="ef62b-164">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-165">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="ef62b-165">-Sku</span></span>
<span data-ttu-id="ef62b-166">Termékváltozat típusa</span><span class="sxs-lookup"><span data-stu-id="ef62b-166">Sku Type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-167">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef62b-167">-SubscriptionId</span></span>
<span data-ttu-id="ef62b-168">Olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="ef62b-168">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ef62b-169">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="ef62b-169">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="ef62b-170">-Tag</span></span>
<span data-ttu-id="ef62b-171">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="ef62b-171">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62b-172">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef62b-172">-Confirm</span></span>
<span data-ttu-id="ef62b-173">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ef62b-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef62b-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef62b-174">-WhatIf</span></span>
<span data-ttu-id="ef62b-175">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ef62b-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef62b-176">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef62b-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef62b-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef62b-177">CommonParameters</span></span>
<span data-ttu-id="ef62b-178">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef62b-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef62b-179">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef62b-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef62b-180">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef62b-180">INPUTS</span></span>

### <span data-ttu-id="ef62b-181">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="ef62b-181">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="ef62b-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef62b-182">OUTPUTS</span></span>

### <span data-ttu-id="ef62b-183">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="ef62b-183">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="ef62b-184">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ef62b-184">NOTES</span></span>

<span data-ttu-id="ef62b-185">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ef62b-185">ALIASES</span></span>

<span data-ttu-id="ef62b-186">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="ef62b-186">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ef62b-187">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="ef62b-187">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ef62b-188">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ef62b-188">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ef62b-189">FORESTTRUST <I ForestTrust[]>: Az Erőforrás-erdő beállításainak listája</span><span class="sxs-lookup"><span data-stu-id="ef62b-189">FORESTTRUST <IForestTrust[]>: List of settings for Resource Forest</span></span>
  - <span data-ttu-id="ef62b-190">`[FriendlyName <String>]`: Rövid név</span><span class="sxs-lookup"><span data-stu-id="ef62b-190">`[FriendlyName <String>]`: Friendly Name</span></span>
  - <span data-ttu-id="ef62b-191">`[RemoteDnsIP <String>]`: Távoli DNS-ips</span><span class="sxs-lookup"><span data-stu-id="ef62b-191">`[RemoteDnsIP <String>]`: Remote Dns ips</span></span>
  - <span data-ttu-id="ef62b-192">`[TrustDirection <String>]`: Megbízhatósági irány</span><span class="sxs-lookup"><span data-stu-id="ef62b-192">`[TrustDirection <String>]`: Trust Direction</span></span>
  - <span data-ttu-id="ef62b-193">`[TrustPassword <String>]`: Megbízható jelszó</span><span class="sxs-lookup"><span data-stu-id="ef62b-193">`[TrustPassword <String>]`: Trust Password</span></span>
  - <span data-ttu-id="ef62b-194">`[TrustedDomainFqdn <String>]`: Megbízható tartomány teljes tartománynév</span><span class="sxs-lookup"><span data-stu-id="ef62b-194">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span></span>

<span data-ttu-id="ef62b-195">INPUTOBJECT: <IAdDomainServicesIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="ef62b-195">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ef62b-196">`[DomainServiceName <String>]`: A tartományszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="ef62b-196">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="ef62b-197">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="ef62b-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ef62b-198">`[ResourceGroupName <String>]`: A felhasználó előfizetésében található erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ef62b-198">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="ef62b-199">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="ef62b-199">The name is case insensitive.</span></span>
  - <span data-ttu-id="ef62b-200">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="ef62b-200">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="ef62b-201">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="ef62b-201">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="ef62b-202">REPLICASET <IReplicaSet[]>: A Replikakészletek listája</span><span class="sxs-lookup"><span data-stu-id="ef62b-202">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span></span>
  - <span data-ttu-id="ef62b-203">`[Location <String>]`: Virtuális hálózati hely</span><span class="sxs-lookup"><span data-stu-id="ef62b-203">`[Location <String>]`: Virtual network location</span></span>
  - <span data-ttu-id="ef62b-204">`[SubnetId <String>]`: Annak a virtuális hálózatnak a neve, amelybe a Domain Services szolgáltatást telepíteni fogja.</span><span class="sxs-lookup"><span data-stu-id="ef62b-204">`[SubnetId <String>]`: The name of the virtual network that Domain Services will be deployed on.</span></span> <span data-ttu-id="ef62b-205">Annak az alhálózatnak az azonosítója, amelybe a Domain Services szolgáltatást telepíteni fogja.</span><span class="sxs-lookup"><span data-stu-id="ef62b-205">The id of the subnet that Domain Services will be deployed on.</span></span> <span data-ttu-id="ef62b-206">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="ef62b-206">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

## <span data-ttu-id="ef62b-207">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef62b-207">RELATED LINKS</span></span>

