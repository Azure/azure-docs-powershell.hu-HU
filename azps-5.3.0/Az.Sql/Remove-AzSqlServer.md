---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
ms.openlocfilehash: 670b3e6ec71a768fe40bbcf542440db5ec685b2f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467100"
---
# <span data-ttu-id="a7425-101">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="a7425-101">Remove-AzSqlServer</span></span>

## <span data-ttu-id="a7425-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7425-102">SYNOPSIS</span></span>
<span data-ttu-id="a7425-103">Eltávolít egy Azure SQL-adatbázis-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="a7425-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="a7425-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a7425-104">SYNTAX</span></span>

```
Remove-AzSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7425-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a7425-105">DESCRIPTION</span></span>
<span data-ttu-id="a7425-106">A **Remove-AzSqlServer** parancsmag eltávolítja az Azure SQL Database-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="a7425-106">The **Remove-AzSqlServer** cmdlet removes an Azure SQL Database server.</span></span>
<span data-ttu-id="a7425-107">A törlési művelet aszinkron, és némi ideig is eltelhet, ezért ellenőrizze, hogy befejeződött-e a művelet, mielőtt végrehajtja a kiszolgáló teljes törlésétől függő további műveleteket.</span><span class="sxs-lookup"><span data-stu-id="a7425-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="a7425-108">Létre kell hoznia például egy új kiszolgálót, amely ugyanazt a nevet használja.</span><span class="sxs-lookup"><span data-stu-id="a7425-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="a7425-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a7425-109">EXAMPLES</span></span>

### <span data-ttu-id="a7425-110">1. példa: Kiszolgáló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a7425-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="a7425-111">Ez a parancs eltávolítja a Server01 nevű Azure SQL Database-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="a7425-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="a7425-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7425-112">PARAMETERS</span></span>

### <span data-ttu-id="a7425-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7425-113">-DefaultProfile</span></span>
<span data-ttu-id="a7425-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a7425-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7425-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a7425-115">-Force</span></span>
<span data-ttu-id="a7425-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="a7425-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a7425-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7425-117">-ResourceGroupName</span></span>
<span data-ttu-id="a7425-118">Annak az erőforráscsoportnak a neve, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="a7425-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a7425-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a7425-119">-ServerName</span></span>
<span data-ttu-id="a7425-120">Az eltávolítható kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="a7425-120">Specifies the name of the server to remove.</span></span>

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

### <span data-ttu-id="a7425-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7425-121">-Confirm</span></span>
<span data-ttu-id="a7425-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a7425-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7425-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7425-123">-WhatIf</span></span>
<span data-ttu-id="a7425-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a7425-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7425-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a7425-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7425-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7425-126">CommonParameters</span></span>
<span data-ttu-id="a7425-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7425-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7425-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7425-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7425-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7425-129">INPUTS</span></span>

### <span data-ttu-id="a7425-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a7425-130">System.String</span></span>

## <span data-ttu-id="a7425-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7425-131">OUTPUTS</span></span>

### <span data-ttu-id="a7425-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="a7425-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="a7425-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a7425-133">NOTES</span></span>

## <span data-ttu-id="a7425-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7425-134">RELATED LINKS</span></span>

[<span data-ttu-id="a7425-135">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="a7425-135">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="a7425-136">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="a7425-136">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="a7425-137">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="a7425-137">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="a7425-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a7425-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


