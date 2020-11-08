---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: a2920eb845a162ac83f41e5c8de8c47848485431
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195135"
---
# <span data-ttu-id="7df38-101">Get-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7df38-101">Get-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="7df38-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7df38-102">SYNOPSIS</span></span>
<span data-ttu-id="7df38-103">Az áttetsző adattitkosítás (TDE) oltalmazójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="7df38-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

## <span data-ttu-id="7df38-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7df38-104">SYNTAX</span></span>

```
Get-AzSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7df38-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7df38-105">DESCRIPTION</span></span>
<span data-ttu-id="7df38-106">Az Get-AzSqlServerTransparentDataEncryptionProtector parancsmag információkat kap a TDE-oltalmazóról.</span><span class="sxs-lookup"><span data-stu-id="7df38-106">The Get-AzSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="7df38-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7df38-107">EXAMPLES</span></span>

### <span data-ttu-id="7df38-108">Példa 1: az átlátszó adattitkosítás (TDE) oltalmazó beolvasása</span><span class="sxs-lookup"><span data-stu-id="7df38-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="7df38-109">Ez a parancs a TDE Protector nevű kiszolgálót kapja meg a ContosoServer nevű erőforráscsoport nevű ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7df38-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="7df38-110">ResourceGroupName kiszolgálónév – típus ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="7df38-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="7df38-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="7df38-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="7df38-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7df38-112">PARAMETERS</span></span>

### <span data-ttu-id="7df38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7df38-113">-DefaultProfile</span></span>
<span data-ttu-id="7df38-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7df38-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7df38-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7df38-115">-ResourceGroupName</span></span>
<span data-ttu-id="7df38-116">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7df38-116">The name of the resource group</span></span>

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

### <span data-ttu-id="7df38-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="7df38-117">-ServerName</span></span>
<span data-ttu-id="7df38-118">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="7df38-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="7df38-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7df38-119">-Confirm</span></span>
<span data-ttu-id="7df38-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7df38-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7df38-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7df38-121">-WhatIf</span></span>
<span data-ttu-id="7df38-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7df38-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7df38-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7df38-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7df38-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7df38-124">CommonParameters</span></span>
<span data-ttu-id="7df38-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7df38-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7df38-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7df38-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7df38-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7df38-127">INPUTS</span></span>

### <span data-ttu-id="7df38-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7df38-128">System.String</span></span>

## <span data-ttu-id="7df38-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7df38-129">OUTPUTS</span></span>

### <span data-ttu-id="7df38-130">Microsoft. Azure. Command. SQL. TransparentDataEncryption. Model. AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="7df38-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="7df38-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7df38-131">NOTES</span></span>

## <span data-ttu-id="7df38-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7df38-132">RELATED LINKS</span></span>

[<span data-ttu-id="7df38-133">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="7df38-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)