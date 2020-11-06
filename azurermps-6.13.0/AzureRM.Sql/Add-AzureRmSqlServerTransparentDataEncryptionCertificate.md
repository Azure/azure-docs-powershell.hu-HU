---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/Add-AzureRmSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: 333de53ccd3632188100af7f3fcde10e140537c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499392"
---
# <span data-ttu-id="abb50-101">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="abb50-101">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="abb50-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="abb50-102">SYNOPSIS</span></span>
<span data-ttu-id="abb50-103">Átlátszó adattitkosítási tanúsítvány hozzáadása a megadott SQL Server-példányhoz</span><span class="sxs-lookup"><span data-stu-id="abb50-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abb50-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="abb50-104">SYNTAX</span></span>

### <span data-ttu-id="abb50-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="abb50-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzureRmSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abb50-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="abb50-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzureRmSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abb50-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="abb50-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzureRmSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abb50-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="abb50-108">DESCRIPTION</span></span>
<span data-ttu-id="abb50-109">A Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate a megadott SQL Server-példányhoz hozzáadja az átlátszó adattitkosítási tanúsítványt</span><span class="sxs-lookup"><span data-stu-id="abb50-109">The Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="abb50-110">Példák</span><span class="sxs-lookup"><span data-stu-id="abb50-110">EXAMPLES</span></span>

### <span data-ttu-id="abb50-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="abb50-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzureRmSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="abb50-112">TDE tanúsítvány felvétele SQL Serverbe az erőforráscsoport neve és az SQL-kiszolgáló neve segítségével</span><span class="sxs-lookup"><span data-stu-id="abb50-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="abb50-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="abb50-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzureRmSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzureRmSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="abb50-114">TDE-tanúsítvány felvétele a kiszolgálókra kiszolgálói resourceId használatával</span><span class="sxs-lookup"><span data-stu-id="abb50-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="abb50-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="abb50-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzureRmSqlServer | Add-AzureRmSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="abb50-116">TDE tanúsítvány felvétele az erőforráscsoport összes SQL-kiszolgálójára</span><span class="sxs-lookup"><span data-stu-id="abb50-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="abb50-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="abb50-117">PARAMETERS</span></span>

### <span data-ttu-id="abb50-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abb50-118">-DefaultProfile</span></span>
<span data-ttu-id="abb50-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="abb50-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb50-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="abb50-120">-PassThru</span></span>
<span data-ttu-id="abb50-121">A sikeres végrehajtáskor a hozzáadott tanúsítványállapot-objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="abb50-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="abb50-122">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="abb50-122">-Password</span></span>
<span data-ttu-id="abb50-123">Az átlátszó adattitkosítási tanúsítvány jelszava</span><span class="sxs-lookup"><span data-stu-id="abb50-123">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="abb50-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="abb50-124">-PrivateBlob</span></span>
<span data-ttu-id="abb50-125">A privát blob az átlátszó adattitkosítási tanúsítványhoz</span><span class="sxs-lookup"><span data-stu-id="abb50-125">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="abb50-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abb50-126">-ResourceGroupName</span></span>
<span data-ttu-id="abb50-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="abb50-127">The Resource Group Name</span></span>

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

### <span data-ttu-id="abb50-128">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="abb50-128">-ServerName</span></span>
<span data-ttu-id="abb50-129">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="abb50-129">The Server Name</span></span>

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

### <span data-ttu-id="abb50-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="abb50-130">-SqlServer</span></span>
<span data-ttu-id="abb50-131">Az SQL Server bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="abb50-131">The sql server input object</span></span>

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

### <span data-ttu-id="abb50-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="abb50-132">-SqlServerResourceId</span></span>
<span data-ttu-id="abb50-133">Az SQL Server-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="abb50-133">The sql server resource id</span></span>

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

### <span data-ttu-id="abb50-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="abb50-134">-Confirm</span></span>
<span data-ttu-id="abb50-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="abb50-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abb50-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abb50-136">-WhatIf</span></span>
<span data-ttu-id="abb50-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="abb50-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abb50-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="abb50-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abb50-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb50-139">CommonParameters</span></span>
<span data-ttu-id="abb50-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="abb50-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb50-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abb50-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb50-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="abb50-142">INPUTS</span></span>

### <span data-ttu-id="abb50-143">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="abb50-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="abb50-144">Paraméterek: SqlServer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="abb50-144">Parameters: SqlServer (ByValue)</span></span>

### <span data-ttu-id="abb50-145">System. String</span><span class="sxs-lookup"><span data-stu-id="abb50-145">System.String</span></span>

## <span data-ttu-id="abb50-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abb50-146">OUTPUTS</span></span>

### <span data-ttu-id="abb50-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="abb50-147">System.Boolean</span></span>

## <span data-ttu-id="abb50-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="abb50-148">NOTES</span></span>

## <span data-ttu-id="abb50-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abb50-149">RELATED LINKS</span></span>
