---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 282ef9f77f5902d698353528b10e154eb7fd86ef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374666"
---
# <span data-ttu-id="43c6f-101">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="43c6f-101">New-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="43c6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43c6f-102">SYNOPSIS</span></span>
<span data-ttu-id="43c6f-103">Kommunikációs hivatkozást hoz létre két SQL-adatbázis-kiszolgáló közötti rugalmas adatbázis-tranzakciókhoz.</span><span class="sxs-lookup"><span data-stu-id="43c6f-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

## <span data-ttu-id="43c6f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="43c6f-104">SYNTAX</span></span>

```
New-AzSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43c6f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="43c6f-105">DESCRIPTION</span></span>
<span data-ttu-id="43c6f-106">A **New-AzSqlServerCommunicationLink** parancsmag kommunikációs hivatkozást hoz létre az Azure SQL-adatbázis két logikai kiszolgálója közötti rugalmas adatbázis-tranzakciókhoz.</span><span class="sxs-lookup"><span data-stu-id="43c6f-106">The **New-AzSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="43c6f-107">A rugalmas adatbázis-tranzakciók a párosított kiszolgálók bármelyikében átfoghatja az adatbázisokat.</span><span class="sxs-lookup"><span data-stu-id="43c6f-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="43c6f-108">Egy kiszolgálón több hivatkozást is létrehozhat.</span><span class="sxs-lookup"><span data-stu-id="43c6f-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="43c6f-109">Ezért a rugalmas adatbázis-tranzakciók több kiszolgálón is átfognak.</span><span class="sxs-lookup"><span data-stu-id="43c6f-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="43c6f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="43c6f-110">EXAMPLES</span></span>

### <span data-ttu-id="43c6f-111">1. példa: Kommunikációs hivatkozás létrehozása</span><span class="sxs-lookup"><span data-stu-id="43c6f-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="43c6f-112">Ez a parancs egy Link01 nevű hivatkozást hoz létre a ContosoServer17 és a ContosoServer02 között.</span><span class="sxs-lookup"><span data-stu-id="43c6f-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="43c6f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43c6f-113">PARAMETERS</span></span>

### <span data-ttu-id="43c6f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43c6f-114">-AsJob</span></span>
<span data-ttu-id="43c6f-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="43c6f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43c6f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43c6f-116">-DefaultProfile</span></span>
<span data-ttu-id="43c6f-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="43c6f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43c6f-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="43c6f-118">-LinkName</span></span>
<span data-ttu-id="43c6f-119">A parancsmag által létrehozott kiszolgálói kommunikációs hivatkozás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43c6f-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

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

### <span data-ttu-id="43c6f-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="43c6f-120">-PartnerServer</span></span>
<span data-ttu-id="43c6f-121">Annak a másik kiszolgálónak a nevét adja meg, amely részt vesz a kommunikációs hivatkozásban.</span><span class="sxs-lookup"><span data-stu-id="43c6f-121">Specifies the name of the other server that takes part in this communication link.</span></span>

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

### <span data-ttu-id="43c6f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43c6f-122">-ResourceGroupName</span></span>
<span data-ttu-id="43c6f-123">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a *ServerName* paraméterben megadott kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="43c6f-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="43c6f-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="43c6f-124">-ServerName</span></span>
<span data-ttu-id="43c6f-125">Annak a kiszolgálónak a nevét adja meg, amelyen ez a parancsmag beállítja a kommunikációs hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="43c6f-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="43c6f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43c6f-126">-Confirm</span></span>
<span data-ttu-id="43c6f-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="43c6f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43c6f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43c6f-128">-WhatIf</span></span>
<span data-ttu-id="43c6f-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="43c6f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43c6f-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43c6f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43c6f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43c6f-131">CommonParameters</span></span>
<span data-ttu-id="43c6f-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43c6f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43c6f-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43c6f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43c6f-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43c6f-134">INPUTS</span></span>

### <span data-ttu-id="43c6f-135">System.String</span><span class="sxs-lookup"><span data-stu-id="43c6f-135">System.String</span></span>

## <span data-ttu-id="43c6f-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43c6f-136">OUTPUTS</span></span>

### <span data-ttu-id="43c6f-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="43c6f-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="43c6f-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="43c6f-138">NOTES</span></span>
* <span data-ttu-id="43c6f-139">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, kezelő, sql, adatbázis, mssql</span><span class="sxs-lookup"><span data-stu-id="43c6f-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="43c6f-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43c6f-140">RELATED LINKS</span></span>

[<span data-ttu-id="43c6f-141">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="43c6f-141">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="43c6f-142">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="43c6f-142">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="43c6f-143">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="43c6f-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
