---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e90dac7c55c6edca849c483ccb21d4f37197883a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207967"
---
# <span data-ttu-id="7c339-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="7c339-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="7c339-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c339-102">SYNOPSIS</span></span>
<span data-ttu-id="7c339-103">Áttetsző adattitkosítási tanúsítvány hozzáadása a megadott SQL Server-példányhoz</span><span class="sxs-lookup"><span data-stu-id="7c339-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="7c339-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7c339-104">SYNTAX</span></span>

### <span data-ttu-id="7c339-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="7c339-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c339-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c339-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c339-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c339-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c339-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7c339-108">DESCRIPTION</span></span>
<span data-ttu-id="7c339-109">A Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate hozzáad egy áttetsző adattitkosítási tanúsítványt az adott SQL Server-példányhoz</span><span class="sxs-lookup"><span data-stu-id="7c339-109">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="7c339-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7c339-110">EXAMPLES</span></span>

### <span data-ttu-id="7c339-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7c339-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="7c339-112">TDE-tanúsítvány hozzáadása sql serverhez erőforráscsoport neve és SQL Server-név használatával</span><span class="sxs-lookup"><span data-stu-id="7c339-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="7c339-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="7c339-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="7c339-114">TDE-tanúsítvány hozzáadása a kiszolgálókhoz a kiszolgáló resourceId-jának használatával</span><span class="sxs-lookup"><span data-stu-id="7c339-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="7c339-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="7c339-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzSqlServer | Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="7c339-116">TDE-tanúsítvány hozzáadása egy erőforráscsoport összes sql-kiszolgálóhoz</span><span class="sxs-lookup"><span data-stu-id="7c339-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="7c339-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c339-117">PARAMETERS</span></span>

### <span data-ttu-id="7c339-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c339-118">-DefaultProfile</span></span>
<span data-ttu-id="7c339-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c339-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c339-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c339-120">-PassThru</span></span>
<span data-ttu-id="7c339-121">Sikeres végrehajtáskor visszaadja a felvett tanúsítványobjektumot.</span><span class="sxs-lookup"><span data-stu-id="7c339-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="7c339-122">-Password</span><span class="sxs-lookup"><span data-stu-id="7c339-122">-Password</span></span>
<span data-ttu-id="7c339-123">Az áttetsző adattitkosítási tanúsítvány jelszava</span><span class="sxs-lookup"><span data-stu-id="7c339-123">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="7c339-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="7c339-124">-PrivateBlob</span></span>
<span data-ttu-id="7c339-125">The Private blob for Transparent Data Encryption Certificate</span><span class="sxs-lookup"><span data-stu-id="7c339-125">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="7c339-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c339-126">-ResourceGroupName</span></span>
<span data-ttu-id="7c339-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7c339-127">The Resource Group Name</span></span>

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

### <span data-ttu-id="7c339-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7c339-128">-ServerName</span></span>
<span data-ttu-id="7c339-129">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="7c339-129">The Server Name</span></span>

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

### <span data-ttu-id="7c339-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="7c339-130">-SqlServer</span></span>
<span data-ttu-id="7c339-131">Az sql server bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="7c339-131">The sql server input object</span></span>

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

### <span data-ttu-id="7c339-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="7c339-132">-SqlServerResourceId</span></span>
<span data-ttu-id="7c339-133">Az sql server erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="7c339-133">The sql server resource id</span></span>

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

### <span data-ttu-id="7c339-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c339-134">-Confirm</span></span>
<span data-ttu-id="7c339-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7c339-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c339-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c339-136">-WhatIf</span></span>
<span data-ttu-id="7c339-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7c339-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c339-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7c339-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c339-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c339-139">CommonParameters</span></span>
<span data-ttu-id="7c339-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c339-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c339-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c339-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c339-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c339-142">INPUTS</span></span>

### <span data-ttu-id="7c339-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="7c339-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="7c339-144">System.String</span><span class="sxs-lookup"><span data-stu-id="7c339-144">System.String</span></span>

## <span data-ttu-id="7c339-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c339-145">OUTPUTS</span></span>

### <span data-ttu-id="7c339-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7c339-146">System.Boolean</span></span>

## <span data-ttu-id="7c339-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7c339-147">NOTES</span></span>

## <span data-ttu-id="7c339-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c339-148">RELATED LINKS</span></span>
