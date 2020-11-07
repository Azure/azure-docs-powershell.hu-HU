---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 5d8f67de6b6bbe08a34dad279674b29befaa161c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667351"
---
# <span data-ttu-id="8e6bb-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="8e6bb-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="8e6bb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e6bb-102">SYNOPSIS</span></span>
<span data-ttu-id="8e6bb-103">Létrehoz egy konfigurációs objektumot az SQL Server Key Vault hitelesítő adatairól egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="8e6bb-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="8e6bb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e6bb-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e6bb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e6bb-105">DESCRIPTION</span></span>

## <span data-ttu-id="8e6bb-106">Példák</span><span class="sxs-lookup"><span data-stu-id="8e6bb-106">EXAMPLES</span></span>

## <span data-ttu-id="8e6bb-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e6bb-107">PARAMETERS</span></span>

### <span data-ttu-id="8e6bb-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="8e6bb-108">-AzureKeyVaultUrl</span></span>
<span data-ttu-id="8e6bb-109">Azure Key Vault szolgáltatás URL-címe</span><span class="sxs-lookup"><span data-stu-id="8e6bb-109">Azure Key Vault service URL</span></span>

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

### <span data-ttu-id="8e6bb-110">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="8e6bb-110">-CredentialName</span></span>
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

### <span data-ttu-id="8e6bb-111">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="8e6bb-111">-Enable</span></span>
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

### <span data-ttu-id="8e6bb-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e6bb-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="8e6bb-113">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8e6bb-113">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="8e6bb-114">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="8e6bb-114">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="8e6bb-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8e6bb-115">-Confirm</span></span>
<span data-ttu-id="8e6bb-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8e6bb-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e6bb-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e6bb-117">-WhatIf</span></span>
<span data-ttu-id="8e6bb-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8e6bb-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e6bb-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e6bb-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e6bb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e6bb-120">CommonParameters</span></span>
<span data-ttu-id="8e6bb-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e6bb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e6bb-122">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8e6bb-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e6bb-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e6bb-123">INPUTS</span></span>

### <span data-ttu-id="8e6bb-124">System. String</span><span class="sxs-lookup"><span data-stu-id="8e6bb-124">System.String</span></span>

### <span data-ttu-id="8e6bb-125">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8e6bb-125">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8e6bb-126">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="8e6bb-126">System.Security.SecureString</span></span>

## <span data-ttu-id="8e6bb-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e6bb-127">OUTPUTS</span></span>

### <span data-ttu-id="8e6bb-128">Microsoft. Azure. commands. kiszámítás. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="8e6bb-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="8e6bb-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e6bb-129">NOTES</span></span>

## <span data-ttu-id="8e6bb-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e6bb-130">RELATED LINKS</span></span>
