---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Add-AzSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: beb51449ea0264defe640ba60ad687be405ab669
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923338"
---
# <span data-ttu-id="8f6ab-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="8f6ab-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="8f6ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f6ab-102">SYNOPSIS</span></span>
<span data-ttu-id="8f6ab-103">Áttetsző adattitkosítási tanúsítvány hozzáadása a megadott SQL Server-példányhoz</span><span class="sxs-lookup"><span data-stu-id="8f6ab-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="8f6ab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8f6ab-104">SYNTAX</span></span>

### <span data-ttu-id="8f6ab-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="8f6ab-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6ab-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f6ab-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6ab-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f6ab-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f6ab-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8f6ab-108">DESCRIPTION</span></span>
<span data-ttu-id="8f6ab-109">A Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate hozzáad egy áttetsző adattitkosítási tanúsítványt az adott SQL Server-példányhoz</span><span class="sxs-lookup"><span data-stu-id="8f6ab-109">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="8f6ab-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8f6ab-110">EXAMPLES</span></span>

### <span data-ttu-id="8f6ab-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="8f6ab-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="8f6ab-112">TDE-tanúsítvány hozzáadása sql serverhez erőforráscsoport neve és SQL Server-név használatával</span><span class="sxs-lookup"><span data-stu-id="8f6ab-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="8f6ab-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="8f6ab-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="8f6ab-114">TDE-tanúsítvány hozzáadása a kiszolgálókhoz a kiszolgáló resourceId-jának használatával</span><span class="sxs-lookup"><span data-stu-id="8f6ab-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="8f6ab-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="8f6ab-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzSqlServer | Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="8f6ab-116">TDE-tanúsítvány hozzáadása egy erőforráscsoport összes sql-kiszolgálóhoz</span><span class="sxs-lookup"><span data-stu-id="8f6ab-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="8f6ab-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f6ab-117">PARAMETERS</span></span>

### <span data-ttu-id="8f6ab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f6ab-118">-DefaultProfile</span></span>
<span data-ttu-id="8f6ab-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f6ab-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f6ab-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f6ab-120">-PassThru</span></span>
<span data-ttu-id="8f6ab-121">Sikeres végrehajtáskor visszaadja a felvett tanúsítványobjektumot.</span><span class="sxs-lookup"><span data-stu-id="8f6ab-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="8f6ab-122">-Password</span><span class="sxs-lookup"><span data-stu-id="8f6ab-122">-Password</span></span>
<span data-ttu-id="8f6ab-123">Az áttetsző adattitkosítási tanúsítvány jelszava</span><span class="sxs-lookup"><span data-stu-id="8f6ab-123">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f6ab-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="8f6ab-124">-PrivateBlob</span></span>
<span data-ttu-id="8f6ab-125">The Private blob for Transparent Data Encryption Certificate</span><span class="sxs-lookup"><span data-stu-id="8f6ab-125">The Private blob for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f6ab-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f6ab-126">-ResourceGroupName</span></span>
<span data-ttu-id="8f6ab-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8f6ab-127">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f6ab-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8f6ab-128">-ServerName</span></span>
<span data-ttu-id="8f6ab-129">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="8f6ab-129">The Server Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f6ab-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="8f6ab-130">-SqlServer</span></span>
<span data-ttu-id="8f6ab-131">Az SQL Server bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="8f6ab-131">The sql server input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f6ab-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="8f6ab-132">-SqlServerResourceId</span></span>
<span data-ttu-id="8f6ab-133">Az sql server-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="8f6ab-133">The sql server resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f6ab-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f6ab-134">-Confirm</span></span>
<span data-ttu-id="8f6ab-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8f6ab-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f6ab-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f6ab-136">-WhatIf</span></span>
<span data-ttu-id="8f6ab-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8f6ab-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f6ab-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f6ab-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f6ab-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f6ab-139">CommonParameters</span></span>
<span data-ttu-id="8f6ab-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f6ab-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f6ab-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f6ab-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f6ab-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f6ab-142">INPUTS</span></span>

### <span data-ttu-id="8f6ab-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="8f6ab-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="8f6ab-144">System.String</span><span class="sxs-lookup"><span data-stu-id="8f6ab-144">System.String</span></span>

## <span data-ttu-id="8f6ab-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f6ab-145">OUTPUTS</span></span>

### <span data-ttu-id="8f6ab-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8f6ab-146">System.Boolean</span></span>

## <span data-ttu-id="8f6ab-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8f6ab-147">NOTES</span></span>

## <span data-ttu-id="8f6ab-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f6ab-148">RELATED LINKS</span></span>
