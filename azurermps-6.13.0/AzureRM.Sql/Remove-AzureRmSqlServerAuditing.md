---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 692D0B64-95EB-4D36-975F-65674B3B2F8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 3e43a61c95120b0f07f89e3f3fb64aab2dee8dff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497251"
---
# <span data-ttu-id="0fced-101">Remove-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="0fced-101">Remove-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="0fced-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0fced-102">SYNOPSIS</span></span>
<span data-ttu-id="0fced-103">Megszünteti az SQL Server-alapú naplózást.</span><span class="sxs-lookup"><span data-stu-id="0fced-103">Removes the auditing of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fced-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0fced-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerAuditing [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fced-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0fced-105">DESCRIPTION</span></span>
<span data-ttu-id="0fced-106">A **Remove-AzureRmSqlServerAuditing** parancsmag eltávolítja az Azure SQL Server-kiszolgálók naplózását.</span><span class="sxs-lookup"><span data-stu-id="0fced-106">The **Remove-AzureRmSqlServerAuditing** cmdlet removes the auditing of an Azure SQL server.</span></span>
<span data-ttu-id="0fced-107">A parancsmag használatához adja meg a *ResourceGroupName* és a *kiszolgálónév* paramétert a kiszolgáló azonosítójának megadásához.</span><span class="sxs-lookup"><span data-stu-id="0fced-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="0fced-108">A parancsmag futtatása után az Azure SQL Server-alapú adatbázisok naplózása nem történik meg.</span><span class="sxs-lookup"><span data-stu-id="0fced-108">After you run this cmdlet, auditing of the databases on the Azure SQL server is not performed.</span></span>
<span data-ttu-id="0fced-109">Ha a parancs sikeres, és a *PassThru* paramétert adja meg, a parancsmag egy olyan objektumot ad eredményül, amely leírja a jelenlegi naplózási házirendet és az Azure SQL Server-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="0fced-109">If the command succeeds, and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy and the Azure SQL server identifiers.</span></span>
<span data-ttu-id="0fced-110">A kiszolgálói azonosítók tartalmazzák a **ResourceGroupName** és a **kiszolgálónév** értéket.</span><span class="sxs-lookup"><span data-stu-id="0fced-110">Server identifiers include the **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="0fced-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0fced-111">EXAMPLES</span></span>

### <span data-ttu-id="0fced-112">1. példa: az Azure SQL Server-kiszolgálók naplózásának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0fced-112">Example 1: Remove the auditing of an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlServerAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="0fced-113">Ez a parancs eltávolítja az erőforrás csoport Server01 található összes adatbázis naplózását.</span><span class="sxs-lookup"><span data-stu-id="0fced-113">This command removes the auditing of all the databases located on Server01 in resource group.</span></span>

## <span data-ttu-id="0fced-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0fced-114">PARAMETERS</span></span>

### <span data-ttu-id="0fced-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fced-115">-DefaultProfile</span></span>
<span data-ttu-id="0fced-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0fced-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0fced-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fced-117">-PassThru</span></span>
<span data-ttu-id="0fced-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="0fced-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0fced-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="0fced-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0fced-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fced-120">-ResourceGroupName</span></span>
<span data-ttu-id="0fced-121">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure SQL-kiszolgáló van rendelve.</span><span class="sxs-lookup"><span data-stu-id="0fced-121">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="0fced-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="0fced-122">-ServerName</span></span>
<span data-ttu-id="0fced-123">Az Azure SQL Server nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0fced-123">Specifies the name of the Azure SQL server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fced-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0fced-124">-Confirm</span></span>
<span data-ttu-id="0fced-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0fced-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fced-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fced-126">-WhatIf</span></span>
<span data-ttu-id="0fced-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0fced-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fced-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0fced-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fced-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fced-129">CommonParameters</span></span>
<span data-ttu-id="0fced-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0fced-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fced-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fced-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fced-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fced-132">INPUTS</span></span>

### <span data-ttu-id="0fced-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0fced-133">System.String</span></span>

## <span data-ttu-id="0fced-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fced-134">OUTPUTS</span></span>

### <span data-ttu-id="0fced-135">Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="0fced-135">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="0fced-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0fced-136">NOTES</span></span>

## <span data-ttu-id="0fced-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fced-137">RELATED LINKS</span></span>

[<span data-ttu-id="0fced-138">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="0fced-138">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="0fced-139">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="0fced-139">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="0fced-140">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="0fced-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


