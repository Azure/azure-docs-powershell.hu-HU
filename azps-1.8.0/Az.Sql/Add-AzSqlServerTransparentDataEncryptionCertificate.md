---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: dd134408f45d1c24f3a40366026ab66a54b8ff41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669079"
---
# <span data-ttu-id="0c40f-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="0c40f-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="0c40f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0c40f-102">SYNOPSIS</span></span>
<span data-ttu-id="0c40f-103">Átlátszó adattitkosítási tanúsítvány hozzáadása a megadott SQL Server-példányhoz</span><span class="sxs-lookup"><span data-stu-id="0c40f-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="0c40f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0c40f-104">SYNTAX</span></span>

### <span data-ttu-id="0c40f-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0c40f-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c40f-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c40f-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c40f-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c40f-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c40f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0c40f-108">DESCRIPTION</span></span>
<span data-ttu-id="0c40f-109">A Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate a megadott SQL Server-példányhoz hozzáadja az átlátszó adattitkosítási tanúsítványt</span><span class="sxs-lookup"><span data-stu-id="0c40f-109">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="0c40f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0c40f-110">EXAMPLES</span></span>

### <span data-ttu-id="0c40f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0c40f-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="0c40f-112">TDE tanúsítvány felvétele SQL Serverbe az erőforráscsoport neve és az SQL-kiszolgáló neve segítségével</span><span class="sxs-lookup"><span data-stu-id="0c40f-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="0c40f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="0c40f-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="0c40f-114">TDE-tanúsítvány felvétele a kiszolgálókra kiszolgálói resourceId használatával</span><span class="sxs-lookup"><span data-stu-id="0c40f-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="0c40f-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="0c40f-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzSqlServer | Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="0c40f-116">TDE tanúsítvány felvétele az erőforráscsoport összes SQL-kiszolgálójára</span><span class="sxs-lookup"><span data-stu-id="0c40f-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="0c40f-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0c40f-117">PARAMETERS</span></span>

### <span data-ttu-id="0c40f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c40f-118">-DefaultProfile</span></span>
<span data-ttu-id="0c40f-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c40f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c40f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c40f-120">-PassThru</span></span>
<span data-ttu-id="0c40f-121">A sikeres végrehajtáskor a hozzáadott tanúsítványállapot-objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="0c40f-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="0c40f-122">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="0c40f-122">-Password</span></span>
<span data-ttu-id="0c40f-123">Az átlátszó adattitkosítási tanúsítvány jelszava</span><span class="sxs-lookup"><span data-stu-id="0c40f-123">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="0c40f-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="0c40f-124">-PrivateBlob</span></span>
<span data-ttu-id="0c40f-125">A privát blob az átlátszó adattitkosítási tanúsítványhoz</span><span class="sxs-lookup"><span data-stu-id="0c40f-125">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="0c40f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c40f-126">-ResourceGroupName</span></span>
<span data-ttu-id="0c40f-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0c40f-127">The Resource Group Name</span></span>

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

### <span data-ttu-id="0c40f-128">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="0c40f-128">-ServerName</span></span>
<span data-ttu-id="0c40f-129">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="0c40f-129">The Server Name</span></span>

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

### <span data-ttu-id="0c40f-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="0c40f-130">-SqlServer</span></span>
<span data-ttu-id="0c40f-131">Az SQL Server bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="0c40f-131">The sql server input object</span></span>

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

### <span data-ttu-id="0c40f-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="0c40f-132">-SqlServerResourceId</span></span>
<span data-ttu-id="0c40f-133">Az SQL Server-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="0c40f-133">The sql server resource id</span></span>

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

### <span data-ttu-id="0c40f-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0c40f-134">-Confirm</span></span>
<span data-ttu-id="0c40f-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0c40f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c40f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c40f-136">-WhatIf</span></span>
<span data-ttu-id="0c40f-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0c40f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c40f-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0c40f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c40f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c40f-139">CommonParameters</span></span>
<span data-ttu-id="0c40f-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0c40f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c40f-141">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0c40f-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c40f-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c40f-142">INPUTS</span></span>

### <span data-ttu-id="0c40f-143">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="0c40f-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="0c40f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="0c40f-144">System.String</span></span>

## <span data-ttu-id="0c40f-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c40f-145">OUTPUTS</span></span>

### <span data-ttu-id="0c40f-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0c40f-146">System.Boolean</span></span>

## <span data-ttu-id="0c40f-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0c40f-147">NOTES</span></span>

## <span data-ttu-id="0c40f-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c40f-148">RELATED LINKS</span></span>
