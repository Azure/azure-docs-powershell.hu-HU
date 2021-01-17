---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 8d9214b44d5e408717968d042a1cdb86cd25130a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375310"
---
# <span data-ttu-id="ef961-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="ef961-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="ef961-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef961-102">SYNOPSIS</span></span>
<span data-ttu-id="ef961-103">Letiltja az Azure AD-alapú hitelesítést egy adott SQL Serveren.</span><span class="sxs-lookup"><span data-stu-id="ef961-103">Disables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="ef961-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ef961-104">SYNTAX</span></span>

### <span data-ttu-id="ef961-105">UseResourceGroupAndServerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef961-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef961-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef961-106">UseInputObjectParameterSet</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef961-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef961-107">UserResourceIdParameterSet</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef961-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ef961-108">DESCRIPTION</span></span>
<span data-ttu-id="ef961-109">A **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** parancsmag letiltja az Azure Active Directory (Azure AD) csak hitelesítési követelményét az aktuális előfizetésben lévő AzureSQL-kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="ef961-109">The **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="ef961-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ef961-110">EXAMPLES</span></span>

### <span data-ttu-id="ef961-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="ef961-111">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   False
```

<span data-ttu-id="ef961-112">Ez a parancs letiltja az Azure Active Directory (Azure AD) csak hitelesítési követelményét egy Server01 nevű AzureSQL-kiszolgálóhoz, amely egy ResourceGroup01 nevű erőforráscsoporthoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="ef961-112">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="ef961-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef961-113">PARAMETERS</span></span>

### <span data-ttu-id="ef961-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef961-114">-DefaultProfile</span></span>
<span data-ttu-id="ef961-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef961-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef961-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef961-116">-InputObject</span></span>
<span data-ttu-id="ef961-117">A használni használt SQL Server-objektum.</span><span class="sxs-lookup"><span data-stu-id="ef961-117">The SQL server object to use.</span></span>

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

### <span data-ttu-id="ef961-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef961-118">-ResourceGroupName</span></span>
<span data-ttu-id="ef961-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ef961-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="ef961-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef961-120">-ResourceId</span></span>
<span data-ttu-id="ef961-121">A használni használt példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ef961-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="ef961-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ef961-122">-ServerName</span></span>
<span data-ttu-id="ef961-123">Annak az Azure SQL Servernek a neve, amelyben csak az Azure Active Directory hitelesítés található.</span><span class="sxs-lookup"><span data-stu-id="ef961-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="ef961-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef961-124">-Confirm</span></span>
<span data-ttu-id="ef961-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ef961-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef961-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef961-126">-WhatIf</span></span>
<span data-ttu-id="ef961-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ef961-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef961-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef961-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef961-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef961-129">CommonParameters</span></span>
<span data-ttu-id="ef961-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef961-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef961-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef961-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef961-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef961-132">INPUTS</span></span>

### <span data-ttu-id="ef961-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ef961-133">System.String</span></span>

## <span data-ttu-id="ef961-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef961-134">OUTPUTS</span></span>

### <span data-ttu-id="ef961-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="ef961-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="ef961-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ef961-136">NOTES</span></span>

## <span data-ttu-id="ef961-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef961-137">RELATED LINKS</span></span>

[<span data-ttu-id="ef961-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="ef961-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="ef961-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="ef961-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="ef961-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ef961-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="ef961-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ef961-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="ef961-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="ef961-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)