---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: ac2ec676143ef1179adbfeb793bd787d81e8f435
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493325"
---
# <span data-ttu-id="06a14-101">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="06a14-101">New-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="06a14-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06a14-102">SYNOPSIS</span></span>
<span data-ttu-id="06a14-103">Kommunikációs hivatkozást hoz létre a rugalmas adatbázis-tranzakciókhoz két SQL adatbázis-kiszolgáló között.</span><span class="sxs-lookup"><span data-stu-id="06a14-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06a14-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06a14-104">SYNTAX</span></span>

```
New-AzureRmSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06a14-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="06a14-105">DESCRIPTION</span></span>
<span data-ttu-id="06a14-106">A **New-AzureRmSqlServerCommunicationLink** parancsmag egy kommunikációs hivatkozást hoz létre a rugalmas adatbázis-tranzakciókhoz két logikai kiszolgáló között az Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="06a14-106">The **New-AzureRmSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="06a14-107">A rugalmas adatbázis-tranzakciók a párosított kiszolgálókon is átterjedhetnek az adatbázisokra.</span><span class="sxs-lookup"><span data-stu-id="06a14-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="06a14-108">Egy kiszolgálón több hivatkozást is létrehozhat.</span><span class="sxs-lookup"><span data-stu-id="06a14-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="06a14-109">Ezért a rugalmas adatbázis-tranzakciók nagyobb számú kiszolgálón is átterjedhetnek.</span><span class="sxs-lookup"><span data-stu-id="06a14-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="06a14-110">Példák</span><span class="sxs-lookup"><span data-stu-id="06a14-110">EXAMPLES</span></span>

### <span data-ttu-id="06a14-111">Példa 1: kommunikációs hivatkozás létrehozása</span><span class="sxs-lookup"><span data-stu-id="06a14-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="06a14-112">Ez a parancs létrehoz egy Link01 nevű hivatkozást a ContosoServer17 és a ContosoServer02 között.</span><span class="sxs-lookup"><span data-stu-id="06a14-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="06a14-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06a14-113">PARAMETERS</span></span>

### <span data-ttu-id="06a14-114">-LinkName</span><span class="sxs-lookup"><span data-stu-id="06a14-114">-LinkName</span></span>
<span data-ttu-id="06a14-115">A parancsmag által létrehozott kiszolgáló kommunikációs hivatkozás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06a14-115">Specifies the name of the server communication link that this cmdlet creates.</span></span>

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

### <span data-ttu-id="06a14-116">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="06a14-116">-PartnerServer</span></span>
<span data-ttu-id="06a14-117">Annak a másik kiszolgálónak a neve, amely ebben a kommunikációs hivatkozásban vesz részt.</span><span class="sxs-lookup"><span data-stu-id="06a14-117">Specifies the name of the other server that takes part in this communication link.</span></span>

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

### <span data-ttu-id="06a14-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06a14-118">-ResourceGroupName</span></span>
<span data-ttu-id="06a14-119">Annak az erőforráscsoport a neve, amelyhez a *kiszolgálónév* paraméter által megadott kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="06a14-119">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="06a14-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="06a14-120">-ServerName</span></span>
<span data-ttu-id="06a14-121">Annak a kiszolgálónak a nevét adja meg, amelyen a parancsmag a kommunikációs kapcsolatot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="06a14-121">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="06a14-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="06a14-122">-Confirm</span></span>
<span data-ttu-id="06a14-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="06a14-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06a14-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06a14-124">-WhatIf</span></span>
<span data-ttu-id="06a14-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="06a14-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06a14-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06a14-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06a14-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06a14-127">-DefaultProfile</span></span>
<span data-ttu-id="06a14-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06a14-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06a14-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06a14-129">CommonParameters</span></span>
<span data-ttu-id="06a14-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06a14-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06a14-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06a14-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06a14-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06a14-132">INPUTS</span></span>

## <span data-ttu-id="06a14-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06a14-133">OUTPUTS</span></span>

### <span data-ttu-id="06a14-134">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="06a14-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="06a14-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06a14-135">NOTES</span></span>
* <span data-ttu-id="06a14-136">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, adatbázis, MSSQL</span><span class="sxs-lookup"><span data-stu-id="06a14-136">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="06a14-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06a14-137">RELATED LINKS</span></span>

[<span data-ttu-id="06a14-138">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="06a14-138">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="06a14-139">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="06a14-139">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="06a14-140">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="06a14-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
