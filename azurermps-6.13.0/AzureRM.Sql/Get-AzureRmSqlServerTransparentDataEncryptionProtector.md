---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: 93ab4c51882a4c274fd10727d83f5507c7cfa583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492720"
---
# <span data-ttu-id="aa1a7-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="aa1a7-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="aa1a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa1a7-102">SYNOPSIS</span></span>
<span data-ttu-id="aa1a7-103">Az áttetsző adattitkosítás (TDE) oltalmazójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="aa1a7-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa1a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa1a7-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa1a7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa1a7-105">DESCRIPTION</span></span>
<span data-ttu-id="aa1a7-106">Az Get-AzureRmSqlServerTransparentDataEncryptionProtector parancsmag információkat kap a TDE-oltalmazóról.</span><span class="sxs-lookup"><span data-stu-id="aa1a7-106">The Get-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="aa1a7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aa1a7-107">EXAMPLES</span></span>

### <span data-ttu-id="aa1a7-108">Példa 1: az átlátszó adattitkosítás (TDE) oltalmazó beolvasása</span><span class="sxs-lookup"><span data-stu-id="aa1a7-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzureRmSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="aa1a7-109">Ez a parancs a TDE Protector nevű kiszolgálót kapja meg a ContosoServer nevű erőforráscsoport nevű ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="aa1a7-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="aa1a7-110">ResourceGroupName kiszolgálónév – típus ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="aa1a7-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="aa1a7-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="aa1a7-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="aa1a7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa1a7-112">PARAMETERS</span></span>

### <span data-ttu-id="aa1a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa1a7-113">-DefaultProfile</span></span>
<span data-ttu-id="aa1a7-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="aa1a7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa1a7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa1a7-115">-ResourceGroupName</span></span>
<span data-ttu-id="aa1a7-116">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="aa1a7-116">The name of the resource group</span></span>

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

### <span data-ttu-id="aa1a7-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="aa1a7-117">-ServerName</span></span>
<span data-ttu-id="aa1a7-118">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="aa1a7-118">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa1a7-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aa1a7-119">-Confirm</span></span>
<span data-ttu-id="aa1a7-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aa1a7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa1a7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa1a7-121">-WhatIf</span></span>
<span data-ttu-id="aa1a7-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aa1a7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa1a7-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aa1a7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa1a7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa1a7-124">CommonParameters</span></span>
<span data-ttu-id="aa1a7-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa1a7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa1a7-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa1a7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa1a7-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa1a7-127">INPUTS</span></span>

### <span data-ttu-id="aa1a7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="aa1a7-128">System.String</span></span>

## <span data-ttu-id="aa1a7-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa1a7-129">OUTPUTS</span></span>

### <span data-ttu-id="aa1a7-130">Microsoft. Azure. Command. SQL. TransparentDataEncryption. Model. AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="aa1a7-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="aa1a7-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa1a7-131">NOTES</span></span>

## <span data-ttu-id="aa1a7-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa1a7-132">RELATED LINKS</span></span>

[<span data-ttu-id="aa1a7-133">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="aa1a7-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
