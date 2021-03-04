---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 0b1759d6c2dc364904c50df010e6151351999f8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929714"
---
# <span data-ttu-id="4d0d2-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="4d0d2-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="4d0d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d0d2-102">SYNOPSIS</span></span>
<span data-ttu-id="4d0d2-103">Az Azure AD-hitelesítést csak egy adott SQL Serverhez kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4d0d2-103">Gets Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="4d0d2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4d0d2-104">SYNTAX</span></span>

### <span data-ttu-id="4d0d2-105">UseResourceGroupAndServerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d0d2-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d0d2-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d0d2-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d0d2-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d0d2-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d0d2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4d0d2-108">DESCRIPTION</span></span>
<span data-ttu-id="4d0d2-109">A **Get-AzSqlServerActiveDirectoryOnlyAuthentication** parancsmag csak az Azure Active Directory (Azure AD) hitelesítéskövetelményét kapja meg az aktuális előfizetésben lévő AzureSQL-kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="4d0d2-109">The **Get-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="4d0d2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4d0d2-110">EXAMPLES</span></span>

### <span data-ttu-id="4d0d2-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="4d0d2-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   True
```

<span data-ttu-id="4d0d2-112">Ez a parancs csak az Azure Active Directory (Azure AD) hitelesítését követeli meg egy Server01 nevű AzureSQL-kiszolgálóhoz, amely egy ResourceGroup01 nevű erőforráscsoporthoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="4d0d2-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="4d0d2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d0d2-113">PARAMETERS</span></span>

### <span data-ttu-id="4d0d2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d0d2-114">-DefaultProfile</span></span>
<span data-ttu-id="4d0d2-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d0d2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d0d2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d0d2-116">-InputObject</span></span>
<span data-ttu-id="4d0d2-117">A használni használt SQL Server-objektum.</span><span class="sxs-lookup"><span data-stu-id="4d0d2-117">The SQL server object to use.</span></span>

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

### <span data-ttu-id="4d0d2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d0d2-118">-ResourceGroupName</span></span>
<span data-ttu-id="4d0d2-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4d0d2-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="4d0d2-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d0d2-120">-ResourceId</span></span>
<span data-ttu-id="4d0d2-121">A használni használt példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="4d0d2-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="4d0d2-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4d0d2-122">-ServerName</span></span>
<span data-ttu-id="4d0d2-123">Annak az Azure SQL Servernek a neve, amelyben csak az Azure Active Directory hitelesítés található.</span><span class="sxs-lookup"><span data-stu-id="4d0d2-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="4d0d2-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d0d2-124">-Confirm</span></span>
<span data-ttu-id="4d0d2-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4d0d2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d0d2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d0d2-126">-WhatIf</span></span>
<span data-ttu-id="4d0d2-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4d0d2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d0d2-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4d0d2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d0d2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d0d2-129">CommonParameters</span></span>
<span data-ttu-id="4d0d2-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d0d2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d0d2-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d0d2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d0d2-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d0d2-132">INPUTS</span></span>

### <span data-ttu-id="4d0d2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4d0d2-133">System.String</span></span>

## <span data-ttu-id="4d0d2-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d0d2-134">OUTPUTS</span></span>

### <span data-ttu-id="4d0d2-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="4d0d2-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="4d0d2-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4d0d2-136">NOTES</span></span>

## <span data-ttu-id="4d0d2-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d0d2-137">RELATED LINKS</span></span>

[<span data-ttu-id="4d0d2-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="4d0d2-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="4d0d2-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="4d0d2-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="4d0d2-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="4d0d2-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="4d0d2-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="4d0d2-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="4d0d2-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="4d0d2-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)