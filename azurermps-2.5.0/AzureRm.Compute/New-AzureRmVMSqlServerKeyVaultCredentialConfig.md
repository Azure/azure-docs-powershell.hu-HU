---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
ms.openlocfilehash: ee627065d1d6be8037d1a9b054ec6452b9becb41
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850122"
---
# <span data-ttu-id="52f14-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="52f14-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="52f14-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="52f14-102">SYNOPSIS</span></span>
<span data-ttu-id="52f14-103">Létrehoz egy konfigurációs objektumot az SQL Server Key Vault hitelesítő adatairól egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="52f14-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52f14-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="52f14-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52f14-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="52f14-105">DESCRIPTION</span></span>

## <span data-ttu-id="52f14-106">Példák</span><span class="sxs-lookup"><span data-stu-id="52f14-106">EXAMPLES</span></span>

## <span data-ttu-id="52f14-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="52f14-107">PARAMETERS</span></span>

### <span data-ttu-id="52f14-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="52f14-108">-AzureKeyVaultUrl</span></span>
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

### <span data-ttu-id="52f14-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="52f14-109">-CredentialName</span></span>
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

### <span data-ttu-id="52f14-110">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="52f14-110">-Enable</span></span>
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

### <span data-ttu-id="52f14-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52f14-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="52f14-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="52f14-112">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="52f14-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="52f14-113">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="52f14-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="52f14-114">-Confirm</span></span>
<span data-ttu-id="52f14-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="52f14-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52f14-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52f14-116">-WhatIf</span></span>
<span data-ttu-id="52f14-117">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="52f14-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="52f14-118">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="52f14-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52f14-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f14-119">CommonParameters</span></span>
<span data-ttu-id="52f14-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="52f14-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f14-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52f14-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f14-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="52f14-122">INPUTS</span></span>

### <span data-ttu-id="52f14-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="52f14-123">None</span></span>
<span data-ttu-id="52f14-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="52f14-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="52f14-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52f14-125">OUTPUTS</span></span>

### <span data-ttu-id="52f14-126">Microsoft. Azure. commands. kiszámítás. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="52f14-126">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="52f14-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="52f14-127">NOTES</span></span>

## <span data-ttu-id="52f14-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52f14-128">RELATED LINKS</span></span>

