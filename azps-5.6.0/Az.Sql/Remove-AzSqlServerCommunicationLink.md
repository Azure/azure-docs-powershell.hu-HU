---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
ms.openlocfilehash: ed6f1c2a689ed122ac16004b80f2ab0f0ea2ea3c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940977"
---
# <span data-ttu-id="758d0-101">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="758d0-101">Remove-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="758d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="758d0-102">SYNOPSIS</span></span>
<span data-ttu-id="758d0-103">Törli a két kiszolgáló közötti rugalmas adatbázis-tranzakciók kommunikációs hivatkozását.</span><span class="sxs-lookup"><span data-stu-id="758d0-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

## <span data-ttu-id="758d0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="758d0-104">SYNTAX</span></span>

```
Remove-AzSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="758d0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="758d0-105">DESCRIPTION</span></span>
<span data-ttu-id="758d0-106">A **Remove-AzSqlServerCommunicationLink** parancsmag törli a kiszolgálók közötti kommunikációs hivatkozást az Azure SQL-adatbázisban rugalmas adatbázis-tranzakciókhoz.</span><span class="sxs-lookup"><span data-stu-id="758d0-106">The **Remove-AzSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="758d0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="758d0-107">EXAMPLES</span></span>

### <span data-ttu-id="758d0-108">1. példa: Kommunikációs hivatkozás törlése</span><span class="sxs-lookup"><span data-stu-id="758d0-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="758d0-109">Ez a parancs törli a ContosoServer17 kiszolgálón a Link01 nevű kiszolgáló–kiszolgáló kommunikációs hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="758d0-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="758d0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="758d0-110">PARAMETERS</span></span>

### <span data-ttu-id="758d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="758d0-111">-DefaultProfile</span></span>
<span data-ttu-id="758d0-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="758d0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="758d0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="758d0-113">-Force</span></span>
<span data-ttu-id="758d0-114">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="758d0-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="758d0-115">-LinkName</span><span class="sxs-lookup"><span data-stu-id="758d0-115">-LinkName</span></span>
<span data-ttu-id="758d0-116">A parancsmag által törölt kiszolgálói kommunikációs hivatkozás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="758d0-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="758d0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="758d0-117">-ResourceGroupName</span></span>
<span data-ttu-id="758d0-118">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a *ServerName* paraméterben megadott kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="758d0-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="758d0-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="758d0-119">-ServerName</span></span>
<span data-ttu-id="758d0-120">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="758d0-120">Specifies the name of a server.</span></span>
<span data-ttu-id="758d0-121">Ez a kiszolgáló tartalmazza a parancsmag által törölt kommunikációs hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="758d0-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="758d0-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="758d0-122">-Confirm</span></span>
<span data-ttu-id="758d0-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="758d0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="758d0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="758d0-124">-WhatIf</span></span>
<span data-ttu-id="758d0-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="758d0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="758d0-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="758d0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="758d0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="758d0-127">CommonParameters</span></span>
<span data-ttu-id="758d0-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="758d0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="758d0-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="758d0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="758d0-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="758d0-130">INPUTS</span></span>

### <span data-ttu-id="758d0-131">System.String</span><span class="sxs-lookup"><span data-stu-id="758d0-131">System.String</span></span>

## <span data-ttu-id="758d0-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="758d0-132">OUTPUTS</span></span>

### <span data-ttu-id="758d0-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="758d0-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="758d0-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="758d0-134">NOTES</span></span>
* <span data-ttu-id="758d0-135">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, kezelő, sql, adatbázis, mssql</span><span class="sxs-lookup"><span data-stu-id="758d0-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="758d0-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="758d0-136">RELATED LINKS</span></span>

[<span data-ttu-id="758d0-137">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="758d0-137">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="758d0-138">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="758d0-138">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="758d0-139">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="758d0-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
