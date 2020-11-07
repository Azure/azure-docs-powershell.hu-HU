---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 282ef9f77f5902d698353528b10e154eb7fd86ef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847393"
---
# <span data-ttu-id="df673-101">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="df673-101">New-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="df673-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df673-102">SYNOPSIS</span></span>
<span data-ttu-id="df673-103">Kommunikációs hivatkozást hoz létre a rugalmas adatbázis-tranzakciókhoz két SQL adatbázis-kiszolgáló között.</span><span class="sxs-lookup"><span data-stu-id="df673-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

## <span data-ttu-id="df673-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df673-104">SYNTAX</span></span>

```
New-AzSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df673-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="df673-105">DESCRIPTION</span></span>
<span data-ttu-id="df673-106">A **New-AzSqlServerCommunicationLink** parancsmag egy kommunikációs hivatkozást hoz létre a rugalmas adatbázis-tranzakciókhoz két logikai kiszolgáló között az Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="df673-106">The **New-AzSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="df673-107">A rugalmas adatbázis-tranzakciók a párosított kiszolgálókon is átterjedhetnek az adatbázisokra.</span><span class="sxs-lookup"><span data-stu-id="df673-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="df673-108">Egy kiszolgálón több hivatkozást is létrehozhat.</span><span class="sxs-lookup"><span data-stu-id="df673-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="df673-109">Ezért a rugalmas adatbázis-tranzakciók nagyobb számú kiszolgálón is átterjedhetnek.</span><span class="sxs-lookup"><span data-stu-id="df673-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="df673-110">Példák</span><span class="sxs-lookup"><span data-stu-id="df673-110">EXAMPLES</span></span>

### <span data-ttu-id="df673-111">Példa 1: kommunikációs hivatkozás létrehozása</span><span class="sxs-lookup"><span data-stu-id="df673-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="df673-112">Ez a parancs létrehoz egy Link01 nevű hivatkozást a ContosoServer17 és a ContosoServer02 között.</span><span class="sxs-lookup"><span data-stu-id="df673-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="df673-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df673-113">PARAMETERS</span></span>

### <span data-ttu-id="df673-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df673-114">-AsJob</span></span>
<span data-ttu-id="df673-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="df673-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="df673-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df673-116">-DefaultProfile</span></span>
<span data-ttu-id="df673-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="df673-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df673-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="df673-118">-LinkName</span></span>
<span data-ttu-id="df673-119">A parancsmag által létrehozott kiszolgáló kommunikációs hivatkozás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df673-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

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

### <span data-ttu-id="df673-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="df673-120">-PartnerServer</span></span>
<span data-ttu-id="df673-121">Annak a másik kiszolgálónak a neve, amely ebben a kommunikációs hivatkozásban vesz részt.</span><span class="sxs-lookup"><span data-stu-id="df673-121">Specifies the name of the other server that takes part in this communication link.</span></span>

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

### <span data-ttu-id="df673-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df673-122">-ResourceGroupName</span></span>
<span data-ttu-id="df673-123">Annak az erőforráscsoport a neve, amelyhez a *kiszolgálónév* paraméter által megadott kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="df673-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="df673-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="df673-124">-ServerName</span></span>
<span data-ttu-id="df673-125">Annak a kiszolgálónak a nevét adja meg, amelyen a parancsmag a kommunikációs kapcsolatot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="df673-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="df673-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="df673-126">-Confirm</span></span>
<span data-ttu-id="df673-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="df673-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df673-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df673-128">-WhatIf</span></span>
<span data-ttu-id="df673-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="df673-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df673-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df673-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df673-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df673-131">CommonParameters</span></span>
<span data-ttu-id="df673-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df673-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df673-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="df673-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df673-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df673-134">INPUTS</span></span>

### <span data-ttu-id="df673-135">System. String</span><span class="sxs-lookup"><span data-stu-id="df673-135">System.String</span></span>

## <span data-ttu-id="df673-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df673-136">OUTPUTS</span></span>

### <span data-ttu-id="df673-137">Microsoft. Azure. Command. SQL. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="df673-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="df673-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df673-138">NOTES</span></span>
* <span data-ttu-id="df673-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, adatbázis, MSSQL</span><span class="sxs-lookup"><span data-stu-id="df673-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="df673-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df673-140">RELATED LINKS</span></span>

[<span data-ttu-id="df673-141">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="df673-141">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="df673-142">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="df673-142">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="df673-143">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="df673-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
