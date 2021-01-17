---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 50bf29524e4c16a7a7186a547505f4dcf7dac4e2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465893"
---
# <span data-ttu-id="89df8-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="89df8-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="89df8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89df8-102">SYNOPSIS</span></span>
<span data-ttu-id="89df8-103">Konfigurációs objektumot hoz létre az SQL Server-kulcs tárolójának hitelesítő adataihoz egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="89df8-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="89df8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="89df8-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89df8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="89df8-105">DESCRIPTION</span></span>

## <span data-ttu-id="89df8-106">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="89df8-106">EXAMPLES</span></span>

## <span data-ttu-id="89df8-107">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89df8-107">PARAMETERS</span></span>

### <span data-ttu-id="89df8-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="89df8-108">-AzureKeyVaultUrl</span></span>
<span data-ttu-id="89df8-109">Azure Key Vault szolgáltatás URL-címe</span><span class="sxs-lookup"><span data-stu-id="89df8-109">Azure Key Vault service URL</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89df8-110">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="89df8-110">-CredentialName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89df8-111">-Enable</span><span class="sxs-lookup"><span data-stu-id="89df8-111">-Enable</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89df8-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89df8-112">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89df8-113">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="89df8-113">-ServicePrincipalName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89df8-114">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="89df8-114">-ServicePrincipalSecret</span></span>
```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89df8-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89df8-115">-Confirm</span></span>
<span data-ttu-id="89df8-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="89df8-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89df8-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89df8-117">-WhatIf</span></span>
<span data-ttu-id="89df8-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="89df8-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89df8-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89df8-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89df8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89df8-120">CommonParameters</span></span>
<span data-ttu-id="89df8-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89df8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89df8-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89df8-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89df8-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89df8-123">INPUTS</span></span>

### <span data-ttu-id="89df8-124">System.String</span><span class="sxs-lookup"><span data-stu-id="89df8-124">System.String</span></span>

### <span data-ttu-id="89df8-125">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="89df8-125">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="89df8-126">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="89df8-126">System.Security.SecureString</span></span>

## <span data-ttu-id="89df8-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89df8-127">OUTPUTS</span></span>

### <span data-ttu-id="89df8-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="89df8-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="89df8-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="89df8-129">NOTES</span></span>

## <span data-ttu-id="89df8-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89df8-130">RELATED LINKS</span></span>
