---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 1144108ce4338065183dc31b0f72dbb51dc69d19
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380476"
---
# <span data-ttu-id="a9c7a-101">Update-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="a9c7a-101">Update-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="a9c7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9c7a-102">SYNOPSIS</span></span>
<span data-ttu-id="a9c7a-103">Frissíti az Azure NetApp-fájlok (ANF) active directory-konfigurációját a megadott opcionális módosítókra.</span><span class="sxs-lookup"><span data-stu-id="a9c7a-103">Updates an Azure NetApp Files (ANF) active directory configuration to the optional modifiers provided.</span></span>

## <span data-ttu-id="a9c7a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a9c7a-104">SYNTAX</span></span>

### <span data-ttu-id="a9c7a-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a9c7a-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>] [-Site <String>] [-SmbServerName <String>]
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9c7a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9c7a-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>]
 [-Site <String>] [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9c7a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9c7a-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory [-Dns <String[]>] [-Domain <String>] [-Site <String>]
 [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>]
 [-KdcIP <String>] [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -InputObject <PSNetAppFilesActiveDirectory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9c7a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a9c7a-108">DESCRIPTION</span></span>
<span data-ttu-id="a9c7a-109">Az **Update-AzNetAppFilesAccount** parancsmag módosítja az ANF active directory-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="a9c7a-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF active directory configuration.</span></span>

## <span data-ttu-id="a9c7a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a9c7a-110">EXAMPLES</span></span>

### <span data-ttu-id="a9c7a-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="a9c7a-111">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesActiveDirectory  -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName" -Username $adUsername
```

<span data-ttu-id="a9c7a-112">Ez a parancs frissítést hajt végre az adott Active Directory-konfiguráción, és módosítja a megadott felhasználónevet.</span><span class="sxs-lookup"><span data-stu-id="a9c7a-112">This command performs an update on the given active directory configuration modifying the username to that provided.</span></span>

## <span data-ttu-id="a9c7a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9c7a-113">PARAMETERS</span></span>

### <span data-ttu-id="a9c7a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a9c7a-114">-AccountName</span></span>
<span data-ttu-id="a9c7a-115">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="a9c7a-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9c7a-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="a9c7a-116">-AccountObject</span></span>
<span data-ttu-id="a9c7a-117">Az Active Directory-objektum fiókja</span><span class="sxs-lookup"><span data-stu-id="a9c7a-117">The account for the active directory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9c7a-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="a9c7a-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="a9c7a-119">Az ANF active directory azonosítója</span><span class="sxs-lookup"><span data-stu-id="a9c7a-119">The ID of the ANF active directory</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9c7a-120">-AdName</span><span class="sxs-lookup"><span data-stu-id="a9c7a-120">-AdName</span></span>
<span data-ttu-id="a9c7a-121">Az Active Directory-számítógép neve.</span><span class="sxs-lookup"><span data-stu-id="a9c7a-121">Name of the active directory machine.</span></span>
<span data-ttu-id="a9c7a-122">Ezt a választható paramétert csak kerberos-kötet létrehozásakor használja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="a9c7a-122">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="a9c7a-123">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="a9c7a-123">-BackupOperator</span></span>
<span data-ttu-id="a9c7a-124">Azok a felhasználók, akik hozzá lesznek adva a Beépített biztonságimásolat-operátor active directory-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="a9c7a-124">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="a9c7a-125">Egyedi felhasználónévk listája tartománykihívó nélkül</span><span class="sxs-lookup"><span data-stu-id="a9c7a-125">A list of unique usernames without domain specifier</span></span>

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

### <span data-ttu-id="a9c7a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9c7a-126">-DefaultProfile</span></span>
<span data-ttu-id="a9c7a-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9c7a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9c7a-128">-Dns</span><span class="sxs-lookup"><span data-stu-id="a9c7a-128">-Dns</span></span>
<span data-ttu-id="a9c7a-129">Az Active Directory-tartomány DNS-kiszolgálójának IP-címeinek vesszővel elválasztott listája (csak IPv4 esetén)</span><span class="sxs-lookup"><span data-stu-id="a9c7a-129">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

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

### <span data-ttu-id="a9c7a-130">-Domain</span><span class="sxs-lookup"><span data-stu-id="a9c7a-130">-Domain</span></span>
<span data-ttu-id="a9c7a-131">Az Active Directory-tartomány neve</span><span class="sxs-lookup"><span data-stu-id="a9c7a-131">Name of the Active Directory domain</span></span>

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

### <span data-ttu-id="a9c7a-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9c7a-132">-InputObject</span></span>
<span data-ttu-id="a9c7a-133">Az eltávolítható Active Directory-objektum</span><span class="sxs-lookup"><span data-stu-id="a9c7a-133">The active directory object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9c7a-134">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="a9c7a-134">-KdcIP</span></span>
<span data-ttu-id="a9c7a-135">az Active Directory-számítógép kdc-kiszolgálójának IP-címei.</span><span class="sxs-lookup"><span data-stu-id="a9c7a-135">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="a9c7a-136">Ezt a választható paramétert csak a kerberos kötet létrehozásakor használja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="a9c7a-136">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="a9c7a-137">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="a9c7a-137">-OrganizationalUnit</span></span>
<span data-ttu-id="a9c7a-138">A Szervezeti egység (OU) a Windows Active Directoryban</span><span class="sxs-lookup"><span data-stu-id="a9c7a-138">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="a9c7a-139">-Password</span><span class="sxs-lookup"><span data-stu-id="a9c7a-139">-Password</span></span>
<span data-ttu-id="a9c7a-140">Az Active Directory tartományi rendszergazdájának egyszerű szöveges jelszava, a válaszban az érték van maszkos</span><span class="sxs-lookup"><span data-stu-id="a9c7a-140">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

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

### <span data-ttu-id="a9c7a-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9c7a-141">-ResourceGroupName</span></span>
<span data-ttu-id="a9c7a-142">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="a9c7a-142">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9c7a-143">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="a9c7a-143">-ServerRootCACertificate</span></span>
<span data-ttu-id="a9c7a-144">Ha az LDAP SSL/TLS protokollon keresztül engedélyezve van, az LDAP-ügyfélprogramnak szüksége van a base64 kódolású Active Directory tanúsítványszolgáltatás önaírt legfelső szintű hitelesítésszolgáltatói tanúsítványára, ez az opcionális paraméter csak az LDAP-felhasználóleképezés köteteit használó két protokollhoz használható.</span><span class="sxs-lookup"><span data-stu-id="a9c7a-144">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="a9c7a-145">-Site</span><span class="sxs-lookup"><span data-stu-id="a9c7a-145">-Site</span></span>
<span data-ttu-id="a9c7a-146">Az Active Directory-webhely, a szolgáltatás a tartományvezérlő felderítését a következőre korlátozza:</span><span class="sxs-lookup"><span data-stu-id="a9c7a-146">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="a9c7a-147">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="a9c7a-147">-SmbServerName</span></span>
<span data-ttu-id="a9c7a-148">Az SMB-kiszolgáló Net ÖSSZES. neve.</span><span class="sxs-lookup"><span data-stu-id="a9c7a-148">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="a9c7a-149">Ez a név lesz regisztrálva számítógépfiókként az AD-ban, és a kötetek csatlakoztatásakor használatos.</span><span class="sxs-lookup"><span data-stu-id="a9c7a-149">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

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

### <span data-ttu-id="a9c7a-150">-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="a9c7a-150">-Username</span></span>
<span data-ttu-id="a9c7a-151">Az Active Directory tartományi rendszergazdájának felhasználóneve</span><span class="sxs-lookup"><span data-stu-id="a9c7a-151">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="a9c7a-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9c7a-152">-Confirm</span></span>
<span data-ttu-id="a9c7a-153">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a9c7a-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9c7a-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9c7a-154">-WhatIf</span></span>
<span data-ttu-id="a9c7a-155">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a9c7a-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9c7a-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a9c7a-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9c7a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9c7a-157">CommonParameters</span></span>
<span data-ttu-id="a9c7a-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9c7a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9c7a-159">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9c7a-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9c7a-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9c7a-160">INPUTS</span></span>

### <span data-ttu-id="a9c7a-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a9c7a-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="a9c7a-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="a9c7a-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="a9c7a-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9c7a-163">OUTPUTS</span></span>

### <span data-ttu-id="a9c7a-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="a9c7a-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="a9c7a-165">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a9c7a-165">NOTES</span></span>

## <span data-ttu-id="a9c7a-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9c7a-166">RELATED LINKS</span></span>
