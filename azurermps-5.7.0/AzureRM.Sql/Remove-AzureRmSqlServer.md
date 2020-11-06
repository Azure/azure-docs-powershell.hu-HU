---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
ms.openlocfilehash: 76b4e024f5a6d5979bbcd9aa860caee823ecc28e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495239"
---
# <span data-ttu-id="02e05-101">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="02e05-101">Remove-AzureRmSqlServer</span></span>

## <span data-ttu-id="02e05-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02e05-102">SYNOPSIS</span></span>
<span data-ttu-id="02e05-103">Azure SQL-adatbázis kiszolgálójának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="02e05-103">Removes an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02e05-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02e05-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02e05-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="02e05-105">DESCRIPTION</span></span>
<span data-ttu-id="02e05-106">A **Remove-AzureRmSqlServer** parancsmag eltávolít egy Azure SQL-adatbázis-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="02e05-106">The **Remove-AzureRmSqlServer** cmdlet removes an Azure SQL Database server.</span></span>

<span data-ttu-id="02e05-107">A törlési művelet aszinkron, és eltarthat egy ideig, ezért ellenőrizheti, hogy a művelet készen áll-e a kiszolgálón a teljes törléstől függő további műveletek elvégzése előtt.</span><span class="sxs-lookup"><span data-stu-id="02e05-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="02e05-108">Például létre kell hoznia egy új kiszolgálót, amely ugyanazt a nevet használja.</span><span class="sxs-lookup"><span data-stu-id="02e05-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="02e05-109">Példák</span><span class="sxs-lookup"><span data-stu-id="02e05-109">EXAMPLES</span></span>

### <span data-ttu-id="02e05-110">1. példa: kiszolgáló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="02e05-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="02e05-111">Ez a parancs eltávolítja a Server01 nevű Azure SQL adatbázis-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="02e05-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="02e05-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02e05-112">PARAMETERS</span></span>

### <span data-ttu-id="02e05-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02e05-113">-DefaultProfile</span></span>
<span data-ttu-id="02e05-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="02e05-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02e05-115">-Force</span><span class="sxs-lookup"><span data-stu-id="02e05-115">-Force</span></span>
<span data-ttu-id="02e05-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="02e05-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="02e05-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02e05-117">-ResourceGroupName</span></span>
<span data-ttu-id="02e05-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="02e05-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="02e05-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="02e05-119">-ServerName</span></span>
<span data-ttu-id="02e05-120">Az eltávolítandó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="02e05-120">Specifies the name of the server to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02e05-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="02e05-121">-Confirm</span></span>
<span data-ttu-id="02e05-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="02e05-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02e05-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02e05-123">-WhatIf</span></span>
<span data-ttu-id="02e05-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="02e05-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02e05-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="02e05-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02e05-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02e05-126">CommonParameters</span></span>
<span data-ttu-id="02e05-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02e05-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02e05-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02e05-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02e05-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02e05-129">INPUTS</span></span>

### <span data-ttu-id="02e05-130">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="02e05-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="02e05-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02e05-131">OUTPUTS</span></span>

### <span data-ttu-id="02e05-132">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="02e05-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="02e05-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02e05-133">NOTES</span></span>

## <span data-ttu-id="02e05-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02e05-134">RELATED LINKS</span></span>

[<span data-ttu-id="02e05-135">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="02e05-135">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="02e05-136">Új – AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="02e05-136">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="02e05-137">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="02e05-137">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="02e05-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="02e05-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


