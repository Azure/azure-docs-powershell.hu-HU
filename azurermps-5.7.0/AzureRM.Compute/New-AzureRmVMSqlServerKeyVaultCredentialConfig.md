---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 4e252001d1459c52a35b766d34c91050df62073d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495447"
---
# <span data-ttu-id="83911-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="83911-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="83911-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83911-102">SYNOPSIS</span></span>
<span data-ttu-id="83911-103">Létrehoz egy konfigurációs objektumot az SQL Server Key Vault hitelesítő adatairól egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="83911-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83911-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83911-104">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83911-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="83911-105">DESCRIPTION</span></span>

## <span data-ttu-id="83911-106">Példák</span><span class="sxs-lookup"><span data-stu-id="83911-106">EXAMPLES</span></span>

## <span data-ttu-id="83911-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83911-107">PARAMETERS</span></span>

### <span data-ttu-id="83911-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="83911-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83911-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="83911-109">-CredentialName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83911-110">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="83911-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83911-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83911-111">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83911-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="83911-112">-ServicePrincipalName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83911-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="83911-113">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83911-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="83911-114">-Confirm</span></span>
<span data-ttu-id="83911-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="83911-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83911-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83911-116">-WhatIf</span></span>
<span data-ttu-id="83911-117">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="83911-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="83911-118">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83911-118">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83911-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83911-119">CommonParameters</span></span>
<span data-ttu-id="83911-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83911-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83911-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83911-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83911-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83911-122">INPUTS</span></span>

### <span data-ttu-id="83911-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="83911-123">None</span></span>
<span data-ttu-id="83911-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="83911-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="83911-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83911-125">OUTPUTS</span></span>

## <span data-ttu-id="83911-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83911-126">NOTES</span></span>

## <span data-ttu-id="83911-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83911-127">RELATED LINKS</span></span>

