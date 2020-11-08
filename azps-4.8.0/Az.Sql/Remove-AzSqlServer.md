---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
ms.openlocfilehash: 670b3e6ec71a768fe40bbcf542440db5ec685b2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181305"
---
# <span data-ttu-id="d83ad-101">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="d83ad-101">Remove-AzSqlServer</span></span>

## <span data-ttu-id="d83ad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d83ad-102">SYNOPSIS</span></span>
<span data-ttu-id="d83ad-103">Azure SQL-adatbázis kiszolgálójának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="d83ad-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="d83ad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d83ad-104">SYNTAX</span></span>

```
Remove-AzSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d83ad-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d83ad-105">DESCRIPTION</span></span>
<span data-ttu-id="d83ad-106">A **Remove-AzSqlServer** parancsmag eltávolít egy Azure SQL-adatbázis-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="d83ad-106">The **Remove-AzSqlServer** cmdlet removes an Azure SQL Database server.</span></span>
<span data-ttu-id="d83ad-107">A törlési művelet aszinkron, és eltarthat egy ideig, ezért ellenőrizheti, hogy a művelet készen áll-e a kiszolgálón a teljes törléstől függő további műveletek elvégzése előtt.</span><span class="sxs-lookup"><span data-stu-id="d83ad-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="d83ad-108">Például létre kell hoznia egy új kiszolgálót, amely ugyanazt a nevet használja.</span><span class="sxs-lookup"><span data-stu-id="d83ad-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="d83ad-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d83ad-109">EXAMPLES</span></span>

### <span data-ttu-id="d83ad-110">1. példa: kiszolgáló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d83ad-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="d83ad-111">Ez a parancs eltávolítja a Server01 nevű Azure SQL adatbázis-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="d83ad-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="d83ad-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d83ad-112">PARAMETERS</span></span>

### <span data-ttu-id="d83ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d83ad-113">-DefaultProfile</span></span>
<span data-ttu-id="d83ad-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d83ad-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d83ad-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d83ad-115">-Force</span></span>
<span data-ttu-id="d83ad-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="d83ad-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d83ad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d83ad-117">-ResourceGroupName</span></span>
<span data-ttu-id="d83ad-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="d83ad-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="d83ad-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="d83ad-119">-ServerName</span></span>
<span data-ttu-id="d83ad-120">Az eltávolítandó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d83ad-120">Specifies the name of the server to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d83ad-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d83ad-121">-Confirm</span></span>
<span data-ttu-id="d83ad-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d83ad-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d83ad-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d83ad-123">-WhatIf</span></span>
<span data-ttu-id="d83ad-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d83ad-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d83ad-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d83ad-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d83ad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d83ad-126">CommonParameters</span></span>
<span data-ttu-id="d83ad-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d83ad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d83ad-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d83ad-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d83ad-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d83ad-129">INPUTS</span></span>

### <span data-ttu-id="d83ad-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d83ad-130">System.String</span></span>

## <span data-ttu-id="d83ad-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d83ad-131">OUTPUTS</span></span>

### <span data-ttu-id="d83ad-132">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="d83ad-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="d83ad-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d83ad-133">NOTES</span></span>

## <span data-ttu-id="d83ad-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d83ad-134">RELATED LINKS</span></span>

[<span data-ttu-id="d83ad-135">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="d83ad-135">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="d83ad-136">Új – AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="d83ad-136">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="d83ad-137">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="d83ad-137">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="d83ad-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d83ad-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


