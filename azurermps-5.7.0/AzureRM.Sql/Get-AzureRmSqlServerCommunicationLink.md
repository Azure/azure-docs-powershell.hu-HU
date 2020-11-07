---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 8240712b4ec6ef17dfff597bed4dc62d60be42b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672350"
---
# <span data-ttu-id="d216c-101">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="d216c-101">Get-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="d216c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d216c-102">SYNOPSIS</span></span>
<span data-ttu-id="d216c-103">Kommunikációs hivatkozásokat kap az adatbázis-kiszolgálók közötti rugalmas adatbázis-tranzakciókban.</span><span class="sxs-lookup"><span data-stu-id="d216c-103">Gets communication links for elastic database transactions between database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d216c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d216c-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d216c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d216c-105">DESCRIPTION</span></span>
<span data-ttu-id="d216c-106">A **Get-AzureRmSqlServerCommunicationLink** parancsmag a kiszolgálók közötti kommunikációs hivatkozásokat kapja meg a rugalmas adatbázis-tranzakciókhoz az Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="d216c-106">The **Get-AzureRmSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="d216c-107">Adja meg a kiszolgáló kommunikációs hivatkozásának nevét a hivatkozás tulajdonságainak megtekintéséhez.</span><span class="sxs-lookup"><span data-stu-id="d216c-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="d216c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d216c-108">EXAMPLES</span></span>

### <span data-ttu-id="d216c-109">Példa 1: a kiszolgáló minden kommunikációs hivatkozásának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d216c-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="d216c-110">Ez a parancs a ContosoServer17 nevű kiszolgáló rugalmas adatbázis-tranzakcióit a kiszolgálók közötti teljes kommunikációs hivatkozással kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d216c-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="d216c-111">2. példa: meghatározott kommunikációs hivatkozás kérése egy kiszolgálóhoz</span><span class="sxs-lookup"><span data-stu-id="d216c-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="d216c-112">Ez a parancs a Link01 nevű kiszolgáló – kiszolgáló kommunikációs hivatkozást kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d216c-112">This command gets the server-to-server communication link named Link01.</span></span>

## <span data-ttu-id="d216c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d216c-113">PARAMETERS</span></span>

### <span data-ttu-id="d216c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d216c-114">-DefaultProfile</span></span>
<span data-ttu-id="d216c-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d216c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d216c-116">-LinkName</span><span class="sxs-lookup"><span data-stu-id="d216c-116">-LinkName</span></span>
<span data-ttu-id="d216c-117">Annak a kiszolgáló-kommunikációs hivatkozásnak a nevét adja meg, amelyre a parancsmag eljut.</span><span class="sxs-lookup"><span data-stu-id="d216c-117">Specifies the name of the server communication link that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d216c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d216c-118">-ResourceGroupName</span></span>
<span data-ttu-id="d216c-119">Annak az erőforráscsoport a neve, amelyhez a *kiszolgálónév* paraméter által megadott kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="d216c-119">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="d216c-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="d216c-120">-ServerName</span></span>
<span data-ttu-id="d216c-121">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d216c-121">Specifies the name of a server.</span></span>
<span data-ttu-id="d216c-122">Ez a kiszolgáló olyan kommunikációs hivatkozást tartalmaz, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="d216c-122">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d216c-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d216c-123">-Confirm</span></span>
<span data-ttu-id="d216c-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d216c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d216c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d216c-125">-WhatIf</span></span>
<span data-ttu-id="d216c-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d216c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d216c-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d216c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d216c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d216c-128">CommonParameters</span></span>
<span data-ttu-id="d216c-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d216c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d216c-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d216c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d216c-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d216c-131">INPUTS</span></span>

### <span data-ttu-id="d216c-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="d216c-132">None</span></span>
<span data-ttu-id="d216c-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d216c-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d216c-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d216c-134">OUTPUTS</span></span>

### <span data-ttu-id="d216c-135">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="d216c-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="d216c-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d216c-136">NOTES</span></span>
* <span data-ttu-id="d216c-137">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, adatbázis, MSSQL</span><span class="sxs-lookup"><span data-stu-id="d216c-137">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="d216c-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d216c-138">RELATED LINKS</span></span>

[<span data-ttu-id="d216c-139">Új – AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="d216c-139">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="d216c-140">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="d216c-140">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="d216c-141">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d216c-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
