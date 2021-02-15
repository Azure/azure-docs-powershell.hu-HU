---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e26d8aa68fd7ffcbab45073b845352feae83aea5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145770"
---
# <span data-ttu-id="6a971-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="6a971-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="6a971-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a971-102">SYNOPSIS</span></span>
<span data-ttu-id="6a971-103">Áttetsző adattitkosítási tanúsítvány hozzáadása a megadott felügyelt példányhoz</span><span class="sxs-lookup"><span data-stu-id="6a971-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="6a971-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6a971-104">SYNTAX</span></span>

```
Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a971-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6a971-105">DESCRIPTION</span></span>
<span data-ttu-id="6a971-106">A Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate hozzáad egy áttetsző adattitkosítási tanúsítványt a megadott felügyelt példányhoz</span><span class="sxs-lookup"><span data-stu-id="6a971-106">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="6a971-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6a971-107">EXAMPLES</span></span>

### <span data-ttu-id="6a971-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="6a971-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="6a971-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a971-109">PARAMETERS</span></span>

### <span data-ttu-id="6a971-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a971-110">-DefaultProfile</span></span>
<span data-ttu-id="6a971-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a971-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a971-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="6a971-112">-ManagedInstanceName</span></span>
<span data-ttu-id="6a971-113">A felügyelt példány neve</span><span class="sxs-lookup"><span data-stu-id="6a971-113">The managed instance name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a971-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a971-114">-PassThru</span></span>
<span data-ttu-id="6a971-115">Sikeres végrehajtáskor visszaadja a felvett tanúsítványobjektumot.</span><span class="sxs-lookup"><span data-stu-id="6a971-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="6a971-116">-Password</span><span class="sxs-lookup"><span data-stu-id="6a971-116">-Password</span></span>
<span data-ttu-id="6a971-117">Az áttetsző adattitkosítási tanúsítvány jelszava</span><span class="sxs-lookup"><span data-stu-id="6a971-117">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a971-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="6a971-118">-PrivateBlob</span></span>
<span data-ttu-id="6a971-119">The Private blob for Transparent Data Encryption Certificate</span><span class="sxs-lookup"><span data-stu-id="6a971-119">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="6a971-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a971-120">-ResourceGroupName</span></span>
<span data-ttu-id="6a971-121">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="6a971-121">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a971-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a971-122">-Confirm</span></span>
<span data-ttu-id="6a971-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6a971-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a971-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a971-124">-WhatIf</span></span>
<span data-ttu-id="6a971-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6a971-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a971-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6a971-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a971-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a971-127">CommonParameters</span></span>
<span data-ttu-id="6a971-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a971-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a971-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a971-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a971-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a971-130">INPUTS</span></span>

### <span data-ttu-id="6a971-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="6a971-131">None</span></span>

## <span data-ttu-id="6a971-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a971-132">OUTPUTS</span></span>

### <span data-ttu-id="6a971-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6a971-133">System.Boolean</span></span>

## <span data-ttu-id="6a971-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6a971-134">NOTES</span></span>

## <span data-ttu-id="6a971-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a971-135">RELATED LINKS</span></span>
