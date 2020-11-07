---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 50bf29524e4c16a7a7186a547505f4dcf7dac4e2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845726"
---
# <span data-ttu-id="6d8f7-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="6d8f7-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="6d8f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6d8f7-102">SYNOPSIS</span></span>
<span data-ttu-id="6d8f7-103">Létrehoz egy konfigurációs objektumot az SQL Server Key Vault hitelesítő adatairól egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="6d8f7-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="6d8f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6d8f7-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d8f7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6d8f7-105">DESCRIPTION</span></span>

## <span data-ttu-id="6d8f7-106">Példák</span><span class="sxs-lookup"><span data-stu-id="6d8f7-106">EXAMPLES</span></span>

## <span data-ttu-id="6d8f7-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6d8f7-107">PARAMETERS</span></span>

### <span data-ttu-id="6d8f7-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="6d8f7-108">-AzureKeyVaultUrl</span></span>
<span data-ttu-id="6d8f7-109">Azure Key Vault szolgáltatás URL-címe</span><span class="sxs-lookup"><span data-stu-id="6d8f7-109">Azure Key Vault service URL</span></span>

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

### <span data-ttu-id="6d8f7-110">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="6d8f7-110">-CredentialName</span></span>
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

### <span data-ttu-id="6d8f7-111">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="6d8f7-111">-Enable</span></span>
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

### <span data-ttu-id="6d8f7-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d8f7-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="6d8f7-113">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="6d8f7-113">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="6d8f7-114">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="6d8f7-114">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="6d8f7-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6d8f7-115">-Confirm</span></span>
<span data-ttu-id="6d8f7-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6d8f7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d8f7-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d8f7-117">-WhatIf</span></span>
<span data-ttu-id="6d8f7-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6d8f7-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d8f7-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6d8f7-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d8f7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d8f7-120">CommonParameters</span></span>
<span data-ttu-id="6d8f7-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6d8f7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d8f7-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6d8f7-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d8f7-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d8f7-123">INPUTS</span></span>

### <span data-ttu-id="6d8f7-124">System. String</span><span class="sxs-lookup"><span data-stu-id="6d8f7-124">System.String</span></span>

### <span data-ttu-id="6d8f7-125">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6d8f7-125">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6d8f7-126">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="6d8f7-126">System.Security.SecureString</span></span>

## <span data-ttu-id="6d8f7-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d8f7-127">OUTPUTS</span></span>

### <span data-ttu-id="6d8f7-128">Microsoft. Azure. commands. kiszámítás. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="6d8f7-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="6d8f7-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6d8f7-129">NOTES</span></span>

## <span data-ttu-id="6d8f7-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d8f7-130">RELATED LINKS</span></span>
