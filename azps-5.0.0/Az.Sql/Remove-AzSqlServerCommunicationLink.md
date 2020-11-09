---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 064262f16a67920b84ca00803325108cc34e6fe5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302995"
---
# <span data-ttu-id="78b73-101">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="78b73-101">Remove-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="78b73-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78b73-102">SYNOPSIS</span></span>
<span data-ttu-id="78b73-103">Két kiszolgáló közötti rugalmas adatbázis-tranzakciókat tartalmazó kommunikációs hivatkozás törlése</span><span class="sxs-lookup"><span data-stu-id="78b73-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

## <span data-ttu-id="78b73-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78b73-104">SYNTAX</span></span>

```
Remove-AzSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78b73-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="78b73-105">DESCRIPTION</span></span>
<span data-ttu-id="78b73-106">A **Remove-AzSqlServerCommunicationLink** parancsmagja a kiszolgálók közötti kommunikációs hivatkozást törli az Azure SQL-adatbázisokban található rugalmas adatbázis-tranzakciókban.</span><span class="sxs-lookup"><span data-stu-id="78b73-106">The **Remove-AzSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="78b73-107">Példák</span><span class="sxs-lookup"><span data-stu-id="78b73-107">EXAMPLES</span></span>

### <span data-ttu-id="78b73-108">Példa 1: kommunikációs hivatkozás törlése</span><span class="sxs-lookup"><span data-stu-id="78b73-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="78b73-109">Ez a parancs törli a ContosoServer17 nevű Link01-kiszolgálóról származó kapcsolati hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="78b73-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="78b73-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78b73-110">PARAMETERS</span></span>

### <span data-ttu-id="78b73-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78b73-111">-DefaultProfile</span></span>
<span data-ttu-id="78b73-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="78b73-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78b73-113">-Force</span><span class="sxs-lookup"><span data-stu-id="78b73-113">-Force</span></span>
<span data-ttu-id="78b73-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="78b73-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="78b73-115">-LinkName</span><span class="sxs-lookup"><span data-stu-id="78b73-115">-LinkName</span></span>
<span data-ttu-id="78b73-116">Annak a kiszolgáló-kommunikációs hivatkozásnak a nevét adja meg, amelyre a parancsmag törlődik.</span><span class="sxs-lookup"><span data-stu-id="78b73-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="78b73-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78b73-117">-ResourceGroupName</span></span>
<span data-ttu-id="78b73-118">Annak az erőforráscsoport a neve, amelyhez a *kiszolgálónév* paraméter által megadott kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="78b73-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="78b73-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="78b73-119">-ServerName</span></span>
<span data-ttu-id="78b73-120">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="78b73-120">Specifies the name of a server.</span></span>
<span data-ttu-id="78b73-121">Ebben a kiszolgálón található a parancsmag által törölt kommunikációs hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="78b73-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="78b73-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="78b73-122">-Confirm</span></span>
<span data-ttu-id="78b73-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="78b73-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78b73-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78b73-124">-WhatIf</span></span>
<span data-ttu-id="78b73-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="78b73-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78b73-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="78b73-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78b73-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78b73-127">CommonParameters</span></span>
<span data-ttu-id="78b73-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78b73-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78b73-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="78b73-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78b73-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78b73-130">INPUTS</span></span>

### <span data-ttu-id="78b73-131">System. String</span><span class="sxs-lookup"><span data-stu-id="78b73-131">System.String</span></span>

## <span data-ttu-id="78b73-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78b73-132">OUTPUTS</span></span>

### <span data-ttu-id="78b73-133">Microsoft. Azure. Command. SQL. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="78b73-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="78b73-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78b73-134">NOTES</span></span>
* <span data-ttu-id="78b73-135">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, adatbázis, MSSQL</span><span class="sxs-lookup"><span data-stu-id="78b73-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="78b73-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78b73-136">RELATED LINKS</span></span>

[<span data-ttu-id="78b73-137">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="78b73-137">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="78b73-138">Új – AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="78b73-138">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="78b73-139">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="78b73-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
