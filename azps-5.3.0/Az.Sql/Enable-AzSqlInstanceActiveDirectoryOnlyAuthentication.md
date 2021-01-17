---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 16390d5100892c3fcbc2607e55a33bdce9385579
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375240"
---
# <span data-ttu-id="60963-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="60963-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="60963-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60963-102">SYNOPSIS</span></span>
<span data-ttu-id="60963-103">Engedélyezi az Azure AD-hitelesítést csak egy adott SQL Felügyelt példány esetén.</span><span class="sxs-lookup"><span data-stu-id="60963-103">Enables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="60963-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="60963-104">SYNTAX</span></span>

### <span data-ttu-id="60963-105">UseResourceGroupAndInstanceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="60963-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60963-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60963-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60963-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60963-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60963-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="60963-108">DESCRIPTION</span></span>
<span data-ttu-id="60963-109">Az **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** parancsmag csak az Azure Active Directory (Azure AD) hitelesítését teszi lehetővé az aktuális előfizetésben lévő AzureSQL Felügyelt példányhoz.</span><span class="sxs-lookup"><span data-stu-id="60963-109">The **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="60963-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="60963-110">EXAMPLES</span></span>

### <span data-ttu-id="60963-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="60963-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="60963-112">Ez a parancs csak az Azure Active Directory (Azure AD) hitelesítését teszi lehetővé egy ManagedInstance01 nevű, Az AzureSQL Felügyelt példányhoz, amely egy ResourceGroup01 nevű erőforráscsoporthoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="60963-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="60963-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60963-113">PARAMETERS</span></span>

### <span data-ttu-id="60963-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60963-114">-DefaultProfile</span></span>
<span data-ttu-id="60963-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60963-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60963-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60963-116">-InputObject</span></span>
<span data-ttu-id="60963-117">A használni használt felügyeltpéldány-objektum.</span><span class="sxs-lookup"><span data-stu-id="60963-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="60963-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="60963-118">-InstanceName</span></span>
<span data-ttu-id="60963-119">Az Azure SQL Felügyelt példány neve, amelybe csak az Azure Active Directory hitelesítés van beszúrva.</span><span class="sxs-lookup"><span data-stu-id="60963-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="60963-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60963-120">-ResourceGroupName</span></span>
<span data-ttu-id="60963-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="60963-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="60963-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60963-122">-ResourceId</span></span>
<span data-ttu-id="60963-123">A használni használt példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="60963-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="60963-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60963-124">-Confirm</span></span>
<span data-ttu-id="60963-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="60963-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60963-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60963-126">-WhatIf</span></span>
<span data-ttu-id="60963-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="60963-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60963-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="60963-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60963-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60963-129">CommonParameters</span></span>
<span data-ttu-id="60963-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60963-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60963-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60963-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60963-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60963-132">INPUTS</span></span>

### <span data-ttu-id="60963-133">System.String</span><span class="sxs-lookup"><span data-stu-id="60963-133">System.String</span></span>

## <span data-ttu-id="60963-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60963-134">OUTPUTS</span></span>

### <span data-ttu-id="60963-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="60963-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="60963-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="60963-136">NOTES</span></span>

## <span data-ttu-id="60963-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60963-137">RELATED LINKS</span></span>

[<span data-ttu-id="60963-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="60963-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="60963-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="60963-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="60963-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="60963-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="60963-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="60963-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)