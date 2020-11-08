---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 002dbbf0a5d244f992beb8a6591907a4c38ed6ae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186711"
---
# <span data-ttu-id="ca198-101">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="ca198-101">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="ca198-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca198-102">SYNOPSIS</span></span>
<span data-ttu-id="ca198-103">Engedélyezi az Azure AD only hitelesítést egy adott SQL Server-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="ca198-103">Enables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="ca198-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca198-104">SYNTAX</span></span>

### <span data-ttu-id="ca198-105">UseResourceGroupAndServerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ca198-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca198-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca198-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca198-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca198-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca198-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca198-108">DESCRIPTION</span></span>
<span data-ttu-id="ca198-109">Az **enable-AzSqlServerActiveDirectoryOnlyAuthentication** parancsmag csak az Azure Active Directoryt (Azure ad) engedélyezi az aktuális előfizetéshez tartozó AzureSQL-kiszolgálók hitelesítési követelményeinek.</span><span class="sxs-lookup"><span data-stu-id="ca198-109">The **Enable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="ca198-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ca198-110">EXAMPLES</span></span>

### <span data-ttu-id="ca198-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ca198-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   True
```

<span data-ttu-id="ca198-112">Ez a parancs engedélyezi az Azure Active Directoryt (Azure AD) a ResourceGroup01 nevű Server01 társított AzureSQL-kiszolgáló hitelesítési követelményeinek.</span><span class="sxs-lookup"><span data-stu-id="ca198-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="ca198-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca198-113">PARAMETERS</span></span>

### <span data-ttu-id="ca198-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca198-114">-DefaultProfile</span></span>
<span data-ttu-id="ca198-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca198-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca198-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca198-116">-InputObject</span></span>
<span data-ttu-id="ca198-117">A használni kívánt SQL Server-objektum.</span><span class="sxs-lookup"><span data-stu-id="ca198-117">The SQL server object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca198-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca198-118">-ResourceGroupName</span></span>
<span data-ttu-id="ca198-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ca198-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca198-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca198-120">-ResourceId</span></span>
<span data-ttu-id="ca198-121">A használni kívánt példa erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ca198-121">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca198-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ca198-122">-ServerName</span></span>
<span data-ttu-id="ca198-123">Annak az Azure SQL Server-kiszolgálónak a neve, amelyen az Azure Active Directory csak a hitelesítést használja.</span><span class="sxs-lookup"><span data-stu-id="ca198-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca198-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ca198-124">-Confirm</span></span>
<span data-ttu-id="ca198-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ca198-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca198-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca198-126">-WhatIf</span></span>
<span data-ttu-id="ca198-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ca198-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca198-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ca198-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca198-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca198-129">CommonParameters</span></span>
<span data-ttu-id="ca198-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca198-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca198-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ca198-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca198-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca198-132">INPUTS</span></span>

### <span data-ttu-id="ca198-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ca198-133">System.String</span></span>

## <span data-ttu-id="ca198-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca198-134">OUTPUTS</span></span>

### <span data-ttu-id="ca198-135">Microsoft. Azure. Command. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="ca198-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="ca198-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca198-136">NOTES</span></span>

## <span data-ttu-id="ca198-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca198-137">RELATED LINKS</span></span>

[<span data-ttu-id="ca198-138">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="ca198-138">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="ca198-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="ca198-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="ca198-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ca198-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="ca198-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ca198-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="ca198-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="ca198-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)