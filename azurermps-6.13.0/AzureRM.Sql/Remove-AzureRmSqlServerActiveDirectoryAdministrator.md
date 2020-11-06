---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: c8b186c55161732a014e281162fa5d6131e72115
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502851"
---
# <span data-ttu-id="8db6d-101">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8db6d-101">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="8db6d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8db6d-102">SYNOPSIS</span></span>
<span data-ttu-id="8db6d-103">Az Azure AD Administrator for SQL Server eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="8db6d-103">Removes an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8db6d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8db6d-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8db6d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8db6d-105">DESCRIPTION</span></span>
<span data-ttu-id="8db6d-106">A **Remove-AzureRmSqlServerActiveDirectoryAdministrator** parancsmag eltávolítja az Azure Active Directoryt (Azure ad) a AzureSQL-kiszolgálónak az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="8db6d-106">The **Remove-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="8db6d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8db6d-107">EXAMPLES</span></span>

### <span data-ttu-id="8db6d-108">1. példa: rendszergazda eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8db6d-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="8db6d-109">Ez a parancs eltávolítja az Azure AD administratort az erőforráscsoport ResourceGroup01 társított Server01 nevű kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="8db6d-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="8db6d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8db6d-110">PARAMETERS</span></span>

### <span data-ttu-id="8db6d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8db6d-111">-DefaultProfile</span></span>
<span data-ttu-id="8db6d-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8db6d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8db6d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8db6d-113">-Force</span></span>
<span data-ttu-id="8db6d-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="8db6d-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8db6d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8db6d-115">-ResourceGroupName</span></span>
<span data-ttu-id="8db6d-116">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az SQL-kiszolgáló van rendelve.</span><span class="sxs-lookup"><span data-stu-id="8db6d-116">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="8db6d-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="8db6d-117">-ServerName</span></span>
<span data-ttu-id="8db6d-118">Annak az SQL-kiszolgálónak a neve, amelyhez a parancsmag eltávolítja a rendszergazdát.</span><span class="sxs-lookup"><span data-stu-id="8db6d-118">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

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

### <span data-ttu-id="8db6d-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8db6d-119">-Confirm</span></span>
<span data-ttu-id="8db6d-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8db6d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8db6d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8db6d-121">-WhatIf</span></span>
<span data-ttu-id="8db6d-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8db6d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8db6d-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8db6d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8db6d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8db6d-124">CommonParameters</span></span>
<span data-ttu-id="8db6d-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8db6d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8db6d-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8db6d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8db6d-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8db6d-127">INPUTS</span></span>

### <span data-ttu-id="8db6d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8db6d-128">System.String</span></span>

## <span data-ttu-id="8db6d-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8db6d-129">OUTPUTS</span></span>

### <span data-ttu-id="8db6d-130">Microsoft. Azure. Command. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="8db6d-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="8db6d-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8db6d-131">NOTES</span></span>

## <span data-ttu-id="8db6d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8db6d-132">RELATED LINKS</span></span>

[<span data-ttu-id="8db6d-133">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8db6d-133">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="8db6d-134">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8db6d-134">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="8db6d-135">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="8db6d-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

