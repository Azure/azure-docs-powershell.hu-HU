---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 355690129f8edcda2586d2dfee570254ce44d998
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183238"
---
# <span data-ttu-id="86af0-101">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="86af0-101">Get-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="86af0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86af0-102">SYNOPSIS</span></span>
<span data-ttu-id="86af0-103">Kommunikációs hivatkozásokat kap az adatbázis-kiszolgálók közötti rugalmas adatbázis-tranzakciókban.</span><span class="sxs-lookup"><span data-stu-id="86af0-103">Gets communication links for elastic database transactions between database servers.</span></span>

## <span data-ttu-id="86af0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86af0-104">SYNTAX</span></span>

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86af0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="86af0-105">DESCRIPTION</span></span>
<span data-ttu-id="86af0-106">A **Get-AzSqlServerCommunicationLink** parancsmag a kiszolgálók közötti kommunikációs hivatkozásokat kapja meg a rugalmas adatbázis-tranzakciókhoz az Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="86af0-106">The **Get-AzSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="86af0-107">Adja meg a kiszolgáló kommunikációs hivatkozásának nevét a hivatkozás tulajdonságainak megtekintéséhez.</span><span class="sxs-lookup"><span data-stu-id="86af0-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="86af0-108">Példák</span><span class="sxs-lookup"><span data-stu-id="86af0-108">EXAMPLES</span></span>

### <span data-ttu-id="86af0-109">Példa 1: a kiszolgáló minden kommunikációs hivatkozásának beszerzése</span><span class="sxs-lookup"><span data-stu-id="86af0-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="86af0-110">Ez a parancs a ContosoServer17 nevű kiszolgáló rugalmas adatbázis-tranzakcióit a kiszolgálók közötti teljes kommunikációs hivatkozással kapja meg.</span><span class="sxs-lookup"><span data-stu-id="86af0-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="86af0-111">2. példa: meghatározott kommunikációs hivatkozás kérése egy kiszolgálóhoz</span><span class="sxs-lookup"><span data-stu-id="86af0-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="86af0-112">Ez a parancs a Link01 nevű kiszolgáló – kiszolgáló kommunikációs hivatkozást kapja meg.</span><span class="sxs-lookup"><span data-stu-id="86af0-112">This command gets the server-to-server communication link named Link01.</span></span>

### <span data-ttu-id="86af0-113">3. példa: a kiszolgálók összes kommunikációs hivatkozásának lekérése szűréssel</span><span class="sxs-lookup"><span data-stu-id="86af0-113">Example 3: Get all communication links for a server using filtering</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

<span data-ttu-id="86af0-114">Ez a parancs a "hivatkozással" kezdődő "ContosoServer17" nevű kiszolgálónak a kiszolgálók közötti rugalmas adatbázis-tranzakciókat kapja.</span><span class="sxs-lookup"><span data-stu-id="86af0-114">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17 that start with "Link".</span></span>

## <span data-ttu-id="86af0-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86af0-115">PARAMETERS</span></span>

### <span data-ttu-id="86af0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86af0-116">-DefaultProfile</span></span>
<span data-ttu-id="86af0-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="86af0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86af0-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="86af0-118">-LinkName</span></span>
<span data-ttu-id="86af0-119">Annak a kiszolgáló-kommunikációs hivatkozásnak a nevét adja meg, amelyre a parancsmag eljut.</span><span class="sxs-lookup"><span data-stu-id="86af0-119">Specifies the name of the server communication link that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86af0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86af0-120">-ResourceGroupName</span></span>
<span data-ttu-id="86af0-121">Annak az erőforráscsoport a neve, amelyhez a *kiszolgálónév* paraméter által megadott kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="86af0-121">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="86af0-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="86af0-122">-ServerName</span></span>
<span data-ttu-id="86af0-123">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="86af0-123">Specifies the name of a server.</span></span>
<span data-ttu-id="86af0-124">Ez a kiszolgáló olyan kommunikációs hivatkozást tartalmaz, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="86af0-124">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="86af0-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="86af0-125">-Confirm</span></span>
<span data-ttu-id="86af0-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="86af0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86af0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86af0-127">-WhatIf</span></span>
<span data-ttu-id="86af0-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="86af0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86af0-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86af0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86af0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86af0-130">CommonParameters</span></span>
<span data-ttu-id="86af0-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86af0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86af0-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="86af0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86af0-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86af0-133">INPUTS</span></span>

### <span data-ttu-id="86af0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="86af0-134">System.String</span></span>

## <span data-ttu-id="86af0-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86af0-135">OUTPUTS</span></span>

### <span data-ttu-id="86af0-136">Microsoft. Azure. Command. SQL. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="86af0-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="86af0-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86af0-137">NOTES</span></span>
* <span data-ttu-id="86af0-138">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, adatbázis, MSSQL</span><span class="sxs-lookup"><span data-stu-id="86af0-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="86af0-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86af0-139">RELATED LINKS</span></span>

[<span data-ttu-id="86af0-140">Új – AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="86af0-140">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="86af0-141">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="86af0-141">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="86af0-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="86af0-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
