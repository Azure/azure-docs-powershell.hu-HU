---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e26d8aa68fd7ffcbab45073b845352feae83aea5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332417"
---
# <span data-ttu-id="e7d41-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="e7d41-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="e7d41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7d41-102">SYNOPSIS</span></span>
<span data-ttu-id="e7d41-103">Áttetsző adattitkosítási tanúsítvány hozzáadása a megadott felügyelt példányhoz</span><span class="sxs-lookup"><span data-stu-id="e7d41-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="e7d41-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e7d41-104">SYNTAX</span></span>

```
Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7d41-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e7d41-105">DESCRIPTION</span></span>
<span data-ttu-id="e7d41-106">A Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate hozzáad egy áttetsző adattitkosítási tanúsítványt a megadott felügyelt példányhoz</span><span class="sxs-lookup"><span data-stu-id="e7d41-106">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="e7d41-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e7d41-107">EXAMPLES</span></span>

### <span data-ttu-id="e7d41-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e7d41-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="e7d41-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7d41-109">PARAMETERS</span></span>

### <span data-ttu-id="e7d41-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7d41-110">-DefaultProfile</span></span>
<span data-ttu-id="e7d41-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7d41-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7d41-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="e7d41-112">-ManagedInstanceName</span></span>
<span data-ttu-id="e7d41-113">A felügyelt példány neve</span><span class="sxs-lookup"><span data-stu-id="e7d41-113">The managed instance name</span></span>

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

### <span data-ttu-id="e7d41-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7d41-114">-PassThru</span></span>
<span data-ttu-id="e7d41-115">Sikeres végrehajtáskor visszaadja a felvett tanúsítványobjektumot.</span><span class="sxs-lookup"><span data-stu-id="e7d41-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="e7d41-116">-Password</span><span class="sxs-lookup"><span data-stu-id="e7d41-116">-Password</span></span>
<span data-ttu-id="e7d41-117">Az áttetsző adattitkosítási tanúsítvány jelszava</span><span class="sxs-lookup"><span data-stu-id="e7d41-117">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="e7d41-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="e7d41-118">-PrivateBlob</span></span>
<span data-ttu-id="e7d41-119">The Private blob for Transparent Data Encryption Certificate</span><span class="sxs-lookup"><span data-stu-id="e7d41-119">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="e7d41-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7d41-120">-ResourceGroupName</span></span>
<span data-ttu-id="e7d41-121">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e7d41-121">The Resource Group Name</span></span>

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

### <span data-ttu-id="e7d41-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7d41-122">-Confirm</span></span>
<span data-ttu-id="e7d41-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e7d41-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7d41-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7d41-124">-WhatIf</span></span>
<span data-ttu-id="e7d41-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e7d41-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7d41-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e7d41-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7d41-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7d41-127">CommonParameters</span></span>
<span data-ttu-id="e7d41-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7d41-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7d41-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7d41-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7d41-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7d41-130">INPUTS</span></span>

### <span data-ttu-id="e7d41-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="e7d41-131">None</span></span>

## <span data-ttu-id="e7d41-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7d41-132">OUTPUTS</span></span>

### <span data-ttu-id="e7d41-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e7d41-133">System.Boolean</span></span>

## <span data-ttu-id="e7d41-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e7d41-134">NOTES</span></span>

## <span data-ttu-id="e7d41-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7d41-135">RELATED LINKS</span></span>
