---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 002dbbf0a5d244f992beb8a6591907a4c38ed6ae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375212"
---
# <span data-ttu-id="2e361-101">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="2e361-101">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="2e361-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e361-102">SYNOPSIS</span></span>
<span data-ttu-id="2e361-103">Az Azure AD-hitelesítést csak egy adott SQL Serverhez engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="2e361-103">Enables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="2e361-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2e361-104">SYNTAX</span></span>

### <span data-ttu-id="2e361-105">UseResourceGroupAndServerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e361-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e361-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e361-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e361-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e361-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e361-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2e361-108">DESCRIPTION</span></span>
<span data-ttu-id="2e361-109">Az **Enable-AzSqlServerActiveDirectoryOnlyAuthentication** parancsmag csak az aktuális előfizetésben lévő AzureSQL-kiszolgálóhoz engedélyezi az Azure Active Directory (Azure AD) hitelesítését.</span><span class="sxs-lookup"><span data-stu-id="2e361-109">The **Enable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="2e361-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2e361-110">EXAMPLES</span></span>

### <span data-ttu-id="2e361-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="2e361-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   True
```

<span data-ttu-id="2e361-112">Ez a parancs lehetővé teszi, hogy az Azure Active Directory (Azure AD) csak hitelesítést követel meg egy Server01 nevű AzureSQL-kiszolgálóhoz, amely egy ResourceGroup01 nevű erőforráscsoporthoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="2e361-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="2e361-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e361-113">PARAMETERS</span></span>

### <span data-ttu-id="2e361-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e361-114">-DefaultProfile</span></span>
<span data-ttu-id="2e361-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e361-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e361-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e361-116">-InputObject</span></span>
<span data-ttu-id="2e361-117">A használni használt SQL Server-objektum.</span><span class="sxs-lookup"><span data-stu-id="2e361-117">The SQL server object to use.</span></span>

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

### <span data-ttu-id="2e361-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e361-118">-ResourceGroupName</span></span>
<span data-ttu-id="2e361-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2e361-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="2e361-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e361-120">-ResourceId</span></span>
<span data-ttu-id="2e361-121">A használni használt példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="2e361-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="2e361-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2e361-122">-ServerName</span></span>
<span data-ttu-id="2e361-123">Annak az Azure SQL Servernek a neve, amelyben csak az Azure Active Directory hitelesítés található.</span><span class="sxs-lookup"><span data-stu-id="2e361-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="2e361-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e361-124">-Confirm</span></span>
<span data-ttu-id="2e361-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2e361-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e361-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e361-126">-WhatIf</span></span>
<span data-ttu-id="2e361-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2e361-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e361-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e361-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e361-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e361-129">CommonParameters</span></span>
<span data-ttu-id="2e361-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e361-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e361-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e361-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e361-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e361-132">INPUTS</span></span>

### <span data-ttu-id="2e361-133">System.String</span><span class="sxs-lookup"><span data-stu-id="2e361-133">System.String</span></span>

## <span data-ttu-id="2e361-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e361-134">OUTPUTS</span></span>

### <span data-ttu-id="2e361-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="2e361-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="2e361-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2e361-136">NOTES</span></span>

## <span data-ttu-id="2e361-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e361-137">RELATED LINKS</span></span>

[<span data-ttu-id="2e361-138">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="2e361-138">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="2e361-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="2e361-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="2e361-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="2e361-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="2e361-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="2e361-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="2e361-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="2e361-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)