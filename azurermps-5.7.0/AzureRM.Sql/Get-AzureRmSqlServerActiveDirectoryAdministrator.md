---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: e782ef221474ab3a041fddc7628157fd999796d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494323"
---
# <span data-ttu-id="38b8d-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="38b8d-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="38b8d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38b8d-102">SYNOPSIS</span></span>
<span data-ttu-id="38b8d-103">Információt kap az Azure AD Administrator for SQL Serverről.</span><span class="sxs-lookup"><span data-stu-id="38b8d-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38b8d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38b8d-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38b8d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="38b8d-105">DESCRIPTION</span></span>
<span data-ttu-id="38b8d-106">A **Get-AzureRmSqlServerActiveDirectoryAdministrator** parancsmag információkat kap az Azure Active Directory (Azure ad) rendszergazdájáról az aktuális előfizetéshez tartozó AzureSQL-kiszolgálókon.</span><span class="sxs-lookup"><span data-stu-id="38b8d-106">The **Get-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="38b8d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="38b8d-107">EXAMPLES</span></span>

### <span data-ttu-id="38b8d-108">1. példa: adatok beolvasása a kiszolgáló rendszergazdájával</span><span class="sxs-lookup"><span data-stu-id="38b8d-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="38b8d-109">Ez a parancs információt ad az Azure AD rendszergazdájáról egy olyan Server01 nevű kiszolgálón, amely egy ResourceGroup01 nevű erőforráscsoport nevével van társítva.</span><span class="sxs-lookup"><span data-stu-id="38b8d-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="38b8d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38b8d-110">PARAMETERS</span></span>

### <span data-ttu-id="38b8d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b8d-111">-DefaultProfile</span></span>
<span data-ttu-id="38b8d-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="38b8d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38b8d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38b8d-113">-ResourceGroupName</span></span>
<span data-ttu-id="38b8d-114">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az SQL-kiszolgáló van rendelve.</span><span class="sxs-lookup"><span data-stu-id="38b8d-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="38b8d-115">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="38b8d-115">-ServerName</span></span>
<span data-ttu-id="38b8d-116">Annak az SQL-kiszolgálónak a neve, amelyhez ez a parancsmag információkat kap.</span><span class="sxs-lookup"><span data-stu-id="38b8d-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="38b8d-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="38b8d-117">-Confirm</span></span>
<span data-ttu-id="38b8d-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="38b8d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38b8d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38b8d-119">-WhatIf</span></span>
<span data-ttu-id="38b8d-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="38b8d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38b8d-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="38b8d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38b8d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b8d-122">CommonParameters</span></span>
<span data-ttu-id="38b8d-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38b8d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b8d-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38b8d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b8d-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38b8d-125">INPUTS</span></span>

### <span data-ttu-id="38b8d-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="38b8d-126">None</span></span>
<span data-ttu-id="38b8d-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="38b8d-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="38b8d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38b8d-128">OUTPUTS</span></span>

### <span data-ttu-id="38b8d-129">Microsoft. Azure. Command. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="38b8d-129">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="38b8d-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38b8d-130">NOTES</span></span>

## <span data-ttu-id="38b8d-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38b8d-131">RELATED LINKS</span></span>

[<span data-ttu-id="38b8d-132">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="38b8d-132">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="38b8d-133">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="38b8d-133">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="38b8d-134">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="38b8d-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


