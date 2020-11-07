---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: ecb49271c49e441140a43f8cb8ae5d65be56cd4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679662"
---
# <span data-ttu-id="e3999-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e3999-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="e3999-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3999-102">SYNOPSIS</span></span>
<span data-ttu-id="e3999-103">Az áttetsző adattitkosítás (TDE) oltalmazójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="e3999-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3999-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3999-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3999-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3999-105">DESCRIPTION</span></span>
<span data-ttu-id="e3999-106">Az Get-AzureRmSqlServerTransparentDataEncryptionProtector parancsmag információkat kap a TDE-oltalmazóról.</span><span class="sxs-lookup"><span data-stu-id="e3999-106">The Get-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="e3999-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e3999-107">EXAMPLES</span></span>

### <span data-ttu-id="e3999-108">Példa 1: az átlátszó adattitkosítás (TDE) oltalmazó beolvasása</span><span class="sxs-lookup"><span data-stu-id="e3999-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzureRmSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="e3999-109">Ez a parancs a TDE Protector nevű kiszolgálót kapja meg a ContosoServer nevű erőforráscsoport nevű ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e3999-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>

<span data-ttu-id="e3999-110">ResourceGroupName kiszolgálónév – típus ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="e3999-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="e3999-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="e3999-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="e3999-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3999-112">PARAMETERS</span></span>

### <span data-ttu-id="e3999-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3999-113">-DefaultProfile</span></span>
<span data-ttu-id="e3999-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e3999-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3999-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3999-115">-ResourceGroupName</span></span>
<span data-ttu-id="e3999-116">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e3999-116">The name of the resource group</span></span>

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

### <span data-ttu-id="e3999-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="e3999-117">-ServerName</span></span>
<span data-ttu-id="e3999-118">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="e3999-118">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3999-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e3999-119">-Confirm</span></span>
<span data-ttu-id="e3999-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e3999-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3999-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3999-121">-WhatIf</span></span>
<span data-ttu-id="e3999-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e3999-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3999-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e3999-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3999-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3999-124">CommonParameters</span></span>
<span data-ttu-id="e3999-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3999-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3999-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3999-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3999-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3999-127">INPUTS</span></span>

### <span data-ttu-id="e3999-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e3999-128">System.String</span></span>

## <span data-ttu-id="e3999-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3999-129">OUTPUTS</span></span>

### <span data-ttu-id="e3999-130">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="e3999-130">System.Object</span></span>

## <span data-ttu-id="e3999-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3999-131">NOTES</span></span>

## <span data-ttu-id="e3999-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3999-132">RELATED LINKS</span></span>

[<span data-ttu-id="e3999-133">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="e3999-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
