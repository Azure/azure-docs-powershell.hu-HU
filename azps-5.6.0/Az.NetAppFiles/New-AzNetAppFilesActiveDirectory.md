---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 73d0ae2a4f4595024db3ee5553a446a5832f0476
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926858"
---
# <span data-ttu-id="2c12f-101">New-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="2c12f-101">New-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="2c12f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c12f-102">SYNOPSIS</span></span>
<span data-ttu-id="2c12f-103">Új Azure NetApp-fájlok (ANF) active directory-konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2c12f-103">Creates a new Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="2c12f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2c12f-104">SYNTAX</span></span>

### <span data-ttu-id="2c12f-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2c12f-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String> [-Dns <String[]>]
 -Domain <String> [-Site <String>] -SmbServerName <String> [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c12f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c12f-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesActiveDirectory [-Dns <String[]>] -Domain <String> [-Site <String>] -SmbServerName <String>
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c12f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2c12f-107">DESCRIPTION</span></span>
<span data-ttu-id="2c12f-108">A **New-AzNetAppFilesActiveDirectory** parancsmag létrehoz egy új Active Directory-konfigurációt egy ANF-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="2c12f-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new active directory configuration for an ANF account.</span></span>

## <span data-ttu-id="2c12f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2c12f-109">EXAMPLES</span></span>

### <span data-ttu-id="2c12f-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="2c12f-110">Example 1</span></span>
```powershell
PS C:\> $pwd_secure_string = Read-Host "Enter a Password" -AsSecureString
PS C:\> New-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyADName" -Username "AdUserName -Password $pwd_secure_string -Domain "AdDomain" -Dns "192.0.2.2" -SmbServerName "AdSmbServerName"
```

<span data-ttu-id="2c12f-111">Ez a parancs az AD-jelszót a "MyAnfAccount" ANF-fiók új Active Directory-konfigurációjának szekreats rendszerében kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2c12f-111">This command gets the AD password from promt into a secreates the new Active Directory configuration for the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="2c12f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c12f-112">PARAMETERS</span></span>

### <span data-ttu-id="2c12f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2c12f-113">-AccountName</span></span>
<span data-ttu-id="2c12f-114">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="2c12f-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="2c12f-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="2c12f-115">-AccountObject</span></span>
<span data-ttu-id="2c12f-116">Az új biztonságimásolat-házirend-objektum fiókja</span><span class="sxs-lookup"><span data-stu-id="2c12f-116">The Account for the new Backup Policy object</span></span>

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

### <span data-ttu-id="2c12f-117">-AdName</span><span class="sxs-lookup"><span data-stu-id="2c12f-117">-AdName</span></span>
<span data-ttu-id="2c12f-118">Az Active Directory-számítógép neve.</span><span class="sxs-lookup"><span data-stu-id="2c12f-118">Name of the active directory machine.</span></span>
<span data-ttu-id="2c12f-119">Ezt a választható paramétert csak kerberos-kötet létrehozásakor használja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="2c12f-119">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="2c12f-120">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="2c12f-120">-BackupOperator</span></span>
<span data-ttu-id="2c12f-121">Azok a felhasználók, akik hozzá lesznek adva a Beépített biztonságimásolat-operátor active directory-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="2c12f-121">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="2c12f-122">Egyedi felhasználónévk listája tartománykihívó nélkül</span><span class="sxs-lookup"><span data-stu-id="2c12f-122">A list of unique usernames without domain specifier</span></span>

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

### <span data-ttu-id="2c12f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c12f-123">-DefaultProfile</span></span>
<span data-ttu-id="2c12f-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c12f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c12f-125">-Dns</span><span class="sxs-lookup"><span data-stu-id="2c12f-125">-Dns</span></span>
<span data-ttu-id="2c12f-126">Az Active Directory-tartomány DNS-kiszolgálójának IP-címeinek vesszővel elválasztott listája (csak IPv4 esetén)</span><span class="sxs-lookup"><span data-stu-id="2c12f-126">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

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

### <span data-ttu-id="2c12f-127">-Domain</span><span class="sxs-lookup"><span data-stu-id="2c12f-127">-Domain</span></span>
<span data-ttu-id="2c12f-128">Az Active Directory-tartomány neve</span><span class="sxs-lookup"><span data-stu-id="2c12f-128">Name of the Active Directory domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c12f-129">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="2c12f-129">-KdcIP</span></span>
<span data-ttu-id="2c12f-130">az Active Directory-számítógép kdc-kiszolgálójának IP-címei.</span><span class="sxs-lookup"><span data-stu-id="2c12f-130">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="2c12f-131">Ezt az opcionális paramétert csak kerberos-kötet létrehozásakor használja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="2c12f-131">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="2c12f-132">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="2c12f-132">-OrganizationalUnit</span></span>
<span data-ttu-id="2c12f-133">A Szervezeti egység (OU) a Windows Active Directoryban</span><span class="sxs-lookup"><span data-stu-id="2c12f-133">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="2c12f-134">-Password</span><span class="sxs-lookup"><span data-stu-id="2c12f-134">-Password</span></span>
<span data-ttu-id="2c12f-135">Az Active Directory tartományi rendszergazdájának egyszerű szöveges jelszava, a válaszban az érték van maszkos</span><span class="sxs-lookup"><span data-stu-id="2c12f-135">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

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

### <span data-ttu-id="2c12f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c12f-136">-ResourceGroupName</span></span>
<span data-ttu-id="2c12f-137">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="2c12f-137">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="2c12f-138">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="2c12f-138">-ServerRootCACertificate</span></span>
<span data-ttu-id="2c12f-139">Ha az LDAP SSL/TLS protokollon keresztül engedélyezve van, az LDAP-ügyfélnek a base64 kódolású Active Directory tanúsítványszolgáltatás öna aláírt legfelső szintű hitelesítésszolgáltatói tanúsítványával kell rendelkezik, ez az opcionális paraméter csak az LDAP-felhasználóleképezés köteteit használó két protokollhoz használható.</span><span class="sxs-lookup"><span data-stu-id="2c12f-139">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="2c12f-140">-Site</span><span class="sxs-lookup"><span data-stu-id="2c12f-140">-Site</span></span>
<span data-ttu-id="2c12f-141">Az Active Directory-webhely, a szolgáltatás a tartományvezérlő felderítését a következőre korlátozza:</span><span class="sxs-lookup"><span data-stu-id="2c12f-141">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="2c12f-142">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="2c12f-142">-SmbServerName</span></span>
<span data-ttu-id="2c12f-143">Az SMB-kiszolgáló Net ÖSSZES. neve.</span><span class="sxs-lookup"><span data-stu-id="2c12f-143">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="2c12f-144">Ez a név lesz regisztrálva az AD-ban számítógépfiókként, és a kötetek csatlakoztatásakor használatos.</span><span class="sxs-lookup"><span data-stu-id="2c12f-144">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c12f-145">-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="2c12f-145">-Username</span></span>
<span data-ttu-id="2c12f-146">Az Active Directory tartományi rendszergazda felhasználóneve</span><span class="sxs-lookup"><span data-stu-id="2c12f-146">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="2c12f-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c12f-147">-Confirm</span></span>
<span data-ttu-id="2c12f-148">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2c12f-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c12f-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c12f-149">-WhatIf</span></span>
<span data-ttu-id="2c12f-150">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2c12f-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c12f-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2c12f-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c12f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c12f-152">CommonParameters</span></span>
<span data-ttu-id="2c12f-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c12f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c12f-154">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c12f-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c12f-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c12f-155">INPUTS</span></span>

### <span data-ttu-id="2c12f-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="2c12f-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="2c12f-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c12f-157">OUTPUTS</span></span>

### <span data-ttu-id="2c12f-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="2c12f-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="2c12f-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2c12f-159">NOTES</span></span>

## <span data-ttu-id="2c12f-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c12f-160">RELATED LINKS</span></span>
