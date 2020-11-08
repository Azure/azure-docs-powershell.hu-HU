---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: a736ede2c84b3fbe782928d7cff14a558b69bcdf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012017"
---
# <span data-ttu-id="4552f-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="4552f-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="4552f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4552f-102">SYNOPSIS</span></span>
<span data-ttu-id="4552f-103">Letiltja az Azure AD only hitelesítést egy adott SQL Server-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="4552f-103">Disables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="4552f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4552f-104">SYNTAX</span></span>

```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4552f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4552f-105">DESCRIPTION</span></span>
<span data-ttu-id="4552f-106">A **disable-AzSqlServerActiveDirectoryOnlyAuthentication** parancsmag letiltja az Azure Active Directoryt (Azure ad) az aktuális előfizetéshez tartozó AzureSQL-kiszolgálók hitelesítési követelményeihez.</span><span class="sxs-lookup"><span data-stu-id="4552f-106">The **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="4552f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4552f-107">EXAMPLES</span></span>

### <span data-ttu-id="4552f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4552f-108">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="4552f-109">Ez a parancs letiltja az Azure Active Directoryt (Azure AD) csak a ResourceGroup01 nevű Server01 társított AzureSQL-kiszolgáló hitelesítési követelményét.</span><span class="sxs-lookup"><span data-stu-id="4552f-109">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="4552f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4552f-110">PARAMETERS</span></span>

### <span data-ttu-id="4552f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4552f-111">-DefaultProfile</span></span>
<span data-ttu-id="4552f-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4552f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4552f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4552f-113">-ResourceGroupName</span></span>
<span data-ttu-id="4552f-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4552f-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="4552f-115">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="4552f-115">-ServerName</span></span>
<span data-ttu-id="4552f-116">Annak az Azure SQL-kiszolgálónak a neve, amelyen az Azure Active Directory rendszergazdája be van kapcsolva.</span><span class="sxs-lookup"><span data-stu-id="4552f-116">The name of the Azure SQL Server the Azure Active Directory administrator is in.</span></span>

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

### <span data-ttu-id="4552f-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4552f-117">-Confirm</span></span>
<span data-ttu-id="4552f-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4552f-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4552f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4552f-119">-WhatIf</span></span>
<span data-ttu-id="4552f-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4552f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4552f-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4552f-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4552f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4552f-122">CommonParameters</span></span>
<span data-ttu-id="4552f-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4552f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4552f-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4552f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4552f-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4552f-125">INPUTS</span></span>

### <span data-ttu-id="4552f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4552f-126">System.String</span></span>

## <span data-ttu-id="4552f-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4552f-127">OUTPUTS</span></span>

### <span data-ttu-id="4552f-128">Microsoft. Azure. Command. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="4552f-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="4552f-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4552f-129">NOTES</span></span>

## <span data-ttu-id="4552f-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4552f-130">RELATED LINKS</span></span>

[<span data-ttu-id="4552f-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="4552f-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="4552f-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="4552f-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="4552f-133">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="4552f-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="4552f-134">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="4552f-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
