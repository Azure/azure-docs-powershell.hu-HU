---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 16390d5100892c3fcbc2607e55a33bdce9385579
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155346"
---
# <span data-ttu-id="fd3ce-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="fd3ce-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="fd3ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd3ce-102">SYNOPSIS</span></span>
<span data-ttu-id="fd3ce-103">Engedélyezi az Azure AD-hitelesítést csak egy adott SQL Felügyelt példány esetén.</span><span class="sxs-lookup"><span data-stu-id="fd3ce-103">Enables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="fd3ce-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fd3ce-104">SYNTAX</span></span>

### <span data-ttu-id="fd3ce-105">UseResourceGroupAndInstanceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd3ce-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd3ce-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd3ce-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd3ce-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd3ce-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd3ce-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fd3ce-108">DESCRIPTION</span></span>
<span data-ttu-id="fd3ce-109">Az **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** parancsmag lehetővé teszi, hogy az Azure Active Directory (Azure AD) csak hitelesítési követelményeket lásson egy AzureSQL Felügyelt példányhoz az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="fd3ce-109">The **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="fd3ce-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fd3ce-110">EXAMPLES</span></span>

### <span data-ttu-id="fd3ce-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="fd3ce-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="fd3ce-112">Ez a parancs csak az Azure Active Directory (Azure AD) hitelesítését teszi lehetővé egy ManagedInstance01 nevű, Az AzureSQL Felügyelt példányhoz, amely egy ResourceGroup01 nevű erőforráscsoporthoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="fd3ce-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="fd3ce-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd3ce-113">PARAMETERS</span></span>

### <span data-ttu-id="fd3ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd3ce-114">-DefaultProfile</span></span>
<span data-ttu-id="fd3ce-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd3ce-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd3ce-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd3ce-116">-InputObject</span></span>
<span data-ttu-id="fd3ce-117">A használni használt felügyeltpéldány-objektum.</span><span class="sxs-lookup"><span data-stu-id="fd3ce-117">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd3ce-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="fd3ce-118">-InstanceName</span></span>
<span data-ttu-id="fd3ce-119">Az Azure SQL Felügyelt példány neve, amelybe csak az Azure Active Directory hitelesítés van beszúrva.</span><span class="sxs-lookup"><span data-stu-id="fd3ce-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd3ce-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd3ce-120">-ResourceGroupName</span></span>
<span data-ttu-id="fd3ce-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fd3ce-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd3ce-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd3ce-122">-ResourceId</span></span>
<span data-ttu-id="fd3ce-123">A használni használt példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="fd3ce-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="fd3ce-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd3ce-124">-Confirm</span></span>
<span data-ttu-id="fd3ce-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fd3ce-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd3ce-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd3ce-126">-WhatIf</span></span>
<span data-ttu-id="fd3ce-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fd3ce-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd3ce-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd3ce-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd3ce-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd3ce-129">CommonParameters</span></span>
<span data-ttu-id="fd3ce-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd3ce-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd3ce-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd3ce-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd3ce-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd3ce-132">INPUTS</span></span>

### <span data-ttu-id="fd3ce-133">System.String</span><span class="sxs-lookup"><span data-stu-id="fd3ce-133">System.String</span></span>

## <span data-ttu-id="fd3ce-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd3ce-134">OUTPUTS</span></span>

### <span data-ttu-id="fd3ce-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="fd3ce-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="fd3ce-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fd3ce-136">NOTES</span></span>

## <span data-ttu-id="fd3ce-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd3ce-137">RELATED LINKS</span></span>

[<span data-ttu-id="fd3ce-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="fd3ce-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="fd3ce-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="fd3ce-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="fd3ce-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="fd3ce-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="fd3ce-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="fd3ce-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)