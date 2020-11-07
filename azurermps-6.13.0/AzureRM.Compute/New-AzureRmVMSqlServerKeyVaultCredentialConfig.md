---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: dc1ea08b0770c7438574d4ef2cc6a97cb99f2909
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672995"
---
# <span data-ttu-id="583a5-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="583a5-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="583a5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="583a5-102">SYNOPSIS</span></span>
<span data-ttu-id="583a5-103">Létrehoz egy konfigurációs objektumot az SQL Server Key Vault hitelesítő adatairól egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="583a5-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="583a5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="583a5-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="583a5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="583a5-105">DESCRIPTION</span></span>

## <span data-ttu-id="583a5-106">Példák</span><span class="sxs-lookup"><span data-stu-id="583a5-106">EXAMPLES</span></span>

## <span data-ttu-id="583a5-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="583a5-107">PARAMETERS</span></span>

### <span data-ttu-id="583a5-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="583a5-108">-AzureKeyVaultUrl</span></span>
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

### <span data-ttu-id="583a5-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="583a5-109">-CredentialName</span></span>
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

### <span data-ttu-id="583a5-110">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="583a5-110">-Enable</span></span>
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

### <span data-ttu-id="583a5-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="583a5-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="583a5-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="583a5-112">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="583a5-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="583a5-113">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="583a5-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="583a5-114">-Confirm</span></span>
<span data-ttu-id="583a5-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="583a5-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="583a5-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="583a5-116">-WhatIf</span></span>
<span data-ttu-id="583a5-117">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="583a5-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="583a5-118">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="583a5-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="583a5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="583a5-119">CommonParameters</span></span>
<span data-ttu-id="583a5-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="583a5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="583a5-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="583a5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="583a5-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="583a5-122">INPUTS</span></span>

### <span data-ttu-id="583a5-123">System. String</span><span class="sxs-lookup"><span data-stu-id="583a5-123">System.String</span></span>

### <span data-ttu-id="583a5-124">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="583a5-124">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="583a5-125">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="583a5-125">System.Security.SecureString</span></span>

## <span data-ttu-id="583a5-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="583a5-126">OUTPUTS</span></span>

### <span data-ttu-id="583a5-127">Microsoft. Azure. commands. kiszámítás. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="583a5-127">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="583a5-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="583a5-128">NOTES</span></span>

## <span data-ttu-id="583a5-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="583a5-129">RELATED LINKS</span></span>
