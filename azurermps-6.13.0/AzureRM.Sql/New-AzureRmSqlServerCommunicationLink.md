---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 8b0f66ceb624689ad66a9ab8fa4bbf9d0fcb2391
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492715"
---
# <span data-ttu-id="1f8c9-101">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="1f8c9-101">New-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="1f8c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f8c9-102">SYNOPSIS</span></span>
<span data-ttu-id="1f8c9-103">Kommunikációs hivatkozást hoz létre a rugalmas adatbázis-tranzakciókhoz két SQL adatbázis-kiszolgáló között.</span><span class="sxs-lookup"><span data-stu-id="1f8c9-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f8c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f8c9-104">SYNTAX</span></span>

```
New-AzureRmSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f8c9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f8c9-105">DESCRIPTION</span></span>
<span data-ttu-id="1f8c9-106">A **New-AzureRmSqlServerCommunicationLink** parancsmag egy kommunikációs hivatkozást hoz létre a rugalmas adatbázis-tranzakciókhoz két logikai kiszolgáló között az Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="1f8c9-106">The **New-AzureRmSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="1f8c9-107">A rugalmas adatbázis-tranzakciók a párosított kiszolgálókon is átterjedhetnek az adatbázisokra.</span><span class="sxs-lookup"><span data-stu-id="1f8c9-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="1f8c9-108">Egy kiszolgálón több hivatkozást is létrehozhat.</span><span class="sxs-lookup"><span data-stu-id="1f8c9-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="1f8c9-109">Ezért a rugalmas adatbázis-tranzakciók nagyobb számú kiszolgálón is átterjedhetnek.</span><span class="sxs-lookup"><span data-stu-id="1f8c9-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="1f8c9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1f8c9-110">EXAMPLES</span></span>

### <span data-ttu-id="1f8c9-111">Példa 1: kommunikációs hivatkozás létrehozása</span><span class="sxs-lookup"><span data-stu-id="1f8c9-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="1f8c9-112">Ez a parancs létrehoz egy Link01 nevű hivatkozást a ContosoServer17 és a ContosoServer02 között.</span><span class="sxs-lookup"><span data-stu-id="1f8c9-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="1f8c9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f8c9-113">PARAMETERS</span></span>

### <span data-ttu-id="1f8c9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f8c9-114">-AsJob</span></span>
<span data-ttu-id="1f8c9-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1f8c9-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f8c9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f8c9-116">-DefaultProfile</span></span>
<span data-ttu-id="1f8c9-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1f8c9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f8c9-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="1f8c9-118">-LinkName</span></span>
<span data-ttu-id="1f8c9-119">A parancsmag által létrehozott kiszolgáló kommunikációs hivatkozás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f8c9-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f8c9-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="1f8c9-120">-PartnerServer</span></span>
<span data-ttu-id="1f8c9-121">Annak a másik kiszolgálónak a neve, amely ebben a kommunikációs hivatkozásban vesz részt.</span><span class="sxs-lookup"><span data-stu-id="1f8c9-121">Specifies the name of the other server that takes part in this communication link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f8c9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f8c9-122">-ResourceGroupName</span></span>
<span data-ttu-id="1f8c9-123">Annak az erőforráscsoport a neve, amelyhez a *kiszolgálónév* paraméter által megadott kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="1f8c9-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="1f8c9-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="1f8c9-124">-ServerName</span></span>
<span data-ttu-id="1f8c9-125">Annak a kiszolgálónak a nevét adja meg, amelyen a parancsmag a kommunikációs kapcsolatot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="1f8c9-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="1f8c9-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1f8c9-126">-Confirm</span></span>
<span data-ttu-id="1f8c9-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1f8c9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f8c9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f8c9-128">-WhatIf</span></span>
<span data-ttu-id="1f8c9-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1f8c9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f8c9-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1f8c9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f8c9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f8c9-131">CommonParameters</span></span>
<span data-ttu-id="1f8c9-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f8c9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f8c9-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f8c9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f8c9-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f8c9-134">INPUTS</span></span>

### <span data-ttu-id="1f8c9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1f8c9-135">System.String</span></span>

## <span data-ttu-id="1f8c9-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f8c9-136">OUTPUTS</span></span>

### <span data-ttu-id="1f8c9-137">Microsoft. Azure. Command. SQL. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="1f8c9-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="1f8c9-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f8c9-138">NOTES</span></span>
* <span data-ttu-id="1f8c9-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, adatbázis, MSSQL</span><span class="sxs-lookup"><span data-stu-id="1f8c9-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="1f8c9-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f8c9-140">RELATED LINKS</span></span>

[<span data-ttu-id="1f8c9-141">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="1f8c9-141">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="1f8c9-142">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="1f8c9-142">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="1f8c9-143">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="1f8c9-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
