---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: d9f732a40b61687d7970fdf24f9f9f0f841b2cc7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844461"
---
# <span data-ttu-id="885dc-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="885dc-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="885dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="885dc-102">SYNOPSIS</span></span>
<span data-ttu-id="885dc-103">Létrehoz egy konfigurációs objektumot az SQL Server Key Vault hitelesítő adatairól egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="885dc-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="885dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="885dc-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="885dc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="885dc-105">DESCRIPTION</span></span>

## <span data-ttu-id="885dc-106">Példák</span><span class="sxs-lookup"><span data-stu-id="885dc-106">EXAMPLES</span></span>

## <span data-ttu-id="885dc-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="885dc-107">PARAMETERS</span></span>

### <span data-ttu-id="885dc-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="885dc-108">-AzureKeyVaultUrl</span></span>
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

### <span data-ttu-id="885dc-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="885dc-109">-CredentialName</span></span>
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

### <span data-ttu-id="885dc-110">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="885dc-110">-Enable</span></span>
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

### <span data-ttu-id="885dc-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="885dc-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="885dc-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="885dc-112">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="885dc-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="885dc-113">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="885dc-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="885dc-114">-Confirm</span></span>
<span data-ttu-id="885dc-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="885dc-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="885dc-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="885dc-116">-WhatIf</span></span>
<span data-ttu-id="885dc-117">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="885dc-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="885dc-118">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="885dc-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="885dc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="885dc-119">CommonParameters</span></span>
<span data-ttu-id="885dc-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="885dc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="885dc-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="885dc-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="885dc-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="885dc-122">INPUTS</span></span>

### <span data-ttu-id="885dc-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="885dc-123">None</span></span>
<span data-ttu-id="885dc-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="885dc-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="885dc-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="885dc-125">OUTPUTS</span></span>

### <span data-ttu-id="885dc-126">Microsoft. Azure. commands. kiszámítás. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="885dc-126">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="885dc-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="885dc-127">NOTES</span></span>

## <span data-ttu-id="885dc-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="885dc-128">RELATED LINKS</span></span>

