---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 355690129f8edcda2586d2dfee570254ce44d998
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476669"
---
# <span data-ttu-id="0439d-101">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="0439d-101">Get-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="0439d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0439d-102">SYNOPSIS</span></span>
<span data-ttu-id="0439d-103">Kommunikációs hivatkozásokat kap az adatbázis-kiszolgálók közötti rugalmas adatbázis-tranzakciókhoz.</span><span class="sxs-lookup"><span data-stu-id="0439d-103">Gets communication links for elastic database transactions between database servers.</span></span>

## <span data-ttu-id="0439d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0439d-104">SYNTAX</span></span>

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0439d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0439d-105">DESCRIPTION</span></span>
<span data-ttu-id="0439d-106">A **Get-AzSqlServerCommunicationLink** parancsmag kiszolgáló–kiszolgáló közötti kommunikációs hivatkozásokat kap az Azure SQL-adatbázisban rugalmas adatbázis-tranzakciókhoz.</span><span class="sxs-lookup"><span data-stu-id="0439d-106">The **Get-AzSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="0439d-107">Adja meg a kiszolgáló kommunikációs hivatkozásának nevét a hivatkozás tulajdonságainak a megtekintése érdekében.</span><span class="sxs-lookup"><span data-stu-id="0439d-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="0439d-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0439d-108">EXAMPLES</span></span>

### <span data-ttu-id="0439d-109">1. példa: Kiszolgáló összes kommunikációs hivatkozásának be szereznie</span><span class="sxs-lookup"><span data-stu-id="0439d-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="0439d-110">Ez a parancs a ContosoServer17 nevű kiszolgáló rugalmas adatbázis-tranzakciókhoz kapcsolódó összes kiszolgáló–kiszolgáló közötti kommunikációs hivatkozást beveszi.</span><span class="sxs-lookup"><span data-stu-id="0439d-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="0439d-111">2. példa: Kiszolgáló adott kommunikációs hivatkozásának lekérte</span><span class="sxs-lookup"><span data-stu-id="0439d-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="0439d-112">Ez a parancs a Link01 nevű kiszolgáló–kiszolgáló kommunikációs hivatkozást kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0439d-112">This command gets the server-to-server communication link named Link01.</span></span>

### <span data-ttu-id="0439d-113">3. példa: Kiszolgáló összes kommunikációs hivatkozásának be szereznie szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="0439d-113">Example 3: Get all communication links for a server using filtering</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

<span data-ttu-id="0439d-114">Ez a parancs a ContosoServer17 nevű kiszolgáló rugalmas adatbázis-tranzakciókhoz kapcsolódó, "Link" kezdetű, kiszolgálók közötti kommunikációs hivatkozásokat kap.</span><span class="sxs-lookup"><span data-stu-id="0439d-114">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17 that start with "Link".</span></span>

## <span data-ttu-id="0439d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0439d-115">PARAMETERS</span></span>

### <span data-ttu-id="0439d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0439d-116">-DefaultProfile</span></span>
<span data-ttu-id="0439d-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0439d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0439d-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="0439d-118">-LinkName</span></span>
<span data-ttu-id="0439d-119">A parancsmag kiszolgálói kommunikációs hivatkozásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0439d-119">Specifies the name of the server communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0439d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0439d-120">-ResourceGroupName</span></span>
<span data-ttu-id="0439d-121">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a *ServerName* paraméterben megadott kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="0439d-121">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="0439d-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0439d-122">-ServerName</span></span>
<span data-ttu-id="0439d-123">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0439d-123">Specifies the name of a server.</span></span>
<span data-ttu-id="0439d-124">Ez a kiszolgáló olyan kommunikációs hivatkozást tartalmaz, amely a parancsmaghoz jut.</span><span class="sxs-lookup"><span data-stu-id="0439d-124">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0439d-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0439d-125">-Confirm</span></span>
<span data-ttu-id="0439d-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0439d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0439d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0439d-127">-WhatIf</span></span>
<span data-ttu-id="0439d-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0439d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0439d-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0439d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0439d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0439d-130">CommonParameters</span></span>
<span data-ttu-id="0439d-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0439d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0439d-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0439d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0439d-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0439d-133">INPUTS</span></span>

### <span data-ttu-id="0439d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="0439d-134">System.String</span></span>

## <span data-ttu-id="0439d-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0439d-135">OUTPUTS</span></span>

### <span data-ttu-id="0439d-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="0439d-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="0439d-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0439d-137">NOTES</span></span>
* <span data-ttu-id="0439d-138">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, kezelő, sql, adatbázis, mssql</span><span class="sxs-lookup"><span data-stu-id="0439d-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="0439d-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0439d-139">RELATED LINKS</span></span>

[<span data-ttu-id="0439d-140">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="0439d-140">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="0439d-141">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="0439d-141">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="0439d-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="0439d-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
