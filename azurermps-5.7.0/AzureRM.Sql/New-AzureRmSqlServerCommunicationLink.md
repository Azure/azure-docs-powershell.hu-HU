---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 0492b81e5674ea08ad98dff1fca75335b1ec8fa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498736"
---
# <span data-ttu-id="762bc-101">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="762bc-101">New-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="762bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="762bc-102">SYNOPSIS</span></span>
<span data-ttu-id="762bc-103">Kommunikációs hivatkozást hoz létre a rugalmas adatbázis-tranzakciókhoz két SQL adatbázis-kiszolgáló között.</span><span class="sxs-lookup"><span data-stu-id="762bc-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="762bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="762bc-104">SYNTAX</span></span>

```
New-AzureRmSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="762bc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="762bc-105">DESCRIPTION</span></span>
<span data-ttu-id="762bc-106">A **New-AzureRmSqlServerCommunicationLink** parancsmag egy kommunikációs hivatkozást hoz létre a rugalmas adatbázis-tranzakciókhoz két logikai kiszolgáló között az Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="762bc-106">The **New-AzureRmSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="762bc-107">A rugalmas adatbázis-tranzakciók a párosított kiszolgálókon is átterjedhetnek az adatbázisokra.</span><span class="sxs-lookup"><span data-stu-id="762bc-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="762bc-108">Egy kiszolgálón több hivatkozást is létrehozhat.</span><span class="sxs-lookup"><span data-stu-id="762bc-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="762bc-109">Ezért a rugalmas adatbázis-tranzakciók nagyobb számú kiszolgálón is átterjedhetnek.</span><span class="sxs-lookup"><span data-stu-id="762bc-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="762bc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="762bc-110">EXAMPLES</span></span>

### <span data-ttu-id="762bc-111">Példa 1: kommunikációs hivatkozás létrehozása</span><span class="sxs-lookup"><span data-stu-id="762bc-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="762bc-112">Ez a parancs létrehoz egy Link01 nevű hivatkozást a ContosoServer17 és a ContosoServer02 között.</span><span class="sxs-lookup"><span data-stu-id="762bc-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="762bc-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="762bc-113">PARAMETERS</span></span>

### <span data-ttu-id="762bc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="762bc-114">-AsJob</span></span>
<span data-ttu-id="762bc-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="762bc-115">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762bc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="762bc-116">-DefaultProfile</span></span>
<span data-ttu-id="762bc-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="762bc-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="762bc-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="762bc-118">-LinkName</span></span>
<span data-ttu-id="762bc-119">A parancsmag által létrehozott kiszolgáló kommunikációs hivatkozás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="762bc-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762bc-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="762bc-120">-PartnerServer</span></span>
<span data-ttu-id="762bc-121">Annak a másik kiszolgálónak a neve, amely ebben a kommunikációs hivatkozásban vesz részt.</span><span class="sxs-lookup"><span data-stu-id="762bc-121">Specifies the name of the other server that takes part in this communication link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762bc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="762bc-122">-ResourceGroupName</span></span>
<span data-ttu-id="762bc-123">Annak az erőforráscsoport a neve, amelyhez a *kiszolgálónév* paraméter által megadott kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="762bc-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="762bc-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="762bc-124">-ServerName</span></span>
<span data-ttu-id="762bc-125">Annak a kiszolgálónak a nevét adja meg, amelyen a parancsmag a kommunikációs kapcsolatot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="762bc-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="762bc-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="762bc-126">-Confirm</span></span>
<span data-ttu-id="762bc-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="762bc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="762bc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="762bc-128">-WhatIf</span></span>
<span data-ttu-id="762bc-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="762bc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="762bc-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="762bc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="762bc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="762bc-131">CommonParameters</span></span>
<span data-ttu-id="762bc-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="762bc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="762bc-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="762bc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="762bc-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="762bc-134">INPUTS</span></span>

### <span data-ttu-id="762bc-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="762bc-135">None</span></span>
<span data-ttu-id="762bc-136">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="762bc-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="762bc-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="762bc-137">OUTPUTS</span></span>

### <span data-ttu-id="762bc-138">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="762bc-138">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="762bc-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="762bc-139">NOTES</span></span>
* <span data-ttu-id="762bc-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, adatbázis, MSSQL</span><span class="sxs-lookup"><span data-stu-id="762bc-140">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="762bc-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="762bc-141">RELATED LINKS</span></span>

[<span data-ttu-id="762bc-142">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="762bc-142">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="762bc-143">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="762bc-143">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="762bc-144">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="762bc-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
