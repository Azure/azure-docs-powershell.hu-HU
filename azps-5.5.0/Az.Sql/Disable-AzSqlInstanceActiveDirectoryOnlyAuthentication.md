---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 5f4ee759fcfddf8e68bc41b68706ccaf2d582e96
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163435"
---
# <span data-ttu-id="e0f9d-101">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="e0f9d-101">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="e0f9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0f9d-102">SYNOPSIS</span></span>
<span data-ttu-id="e0f9d-103">Letiltja az Azure AD-hitelesítést csak egy adott SQL Felügyelt példány esetén.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-103">Disables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="e0f9d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e0f9d-104">SYNTAX</span></span>

### <span data-ttu-id="e0f9d-105">UseResourceGroupAndInstanceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e0f9d-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0f9d-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0f9d-106">UseInputObjectParameterSet</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0f9d-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0f9d-107">UserResourceIdParameterSet</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0f9d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e0f9d-108">DESCRIPTION</span></span>
<span data-ttu-id="e0f9d-109">A **Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication** parancsmag letiltja az Azure Active Directory (Azure AD) csak hitelesítési követelményét egy AzureSQL Felügyelt példány esetében az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-109">The **Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="e0f9d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e0f9d-110">EXAMPLES</span></span>

### <span data-ttu-id="e0f9d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e0f9d-111">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="e0f9d-112">Ez a parancs letiltja az Azure Active Directory (Azure AD) csak hitelesítési követelményét az ResourceGroup01 nevű erőforráscsoporthoz társított ManagedInstance01 nevű AzureSQL Felügyelt példány esetén.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-112">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="e0f9d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0f9d-113">PARAMETERS</span></span>

### <span data-ttu-id="e0f9d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0f9d-114">-DefaultProfile</span></span>
<span data-ttu-id="e0f9d-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0f9d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0f9d-116">-InputObject</span></span>
<span data-ttu-id="e0f9d-117">A használni használt felügyeltpéldány-objektum.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="e0f9d-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e0f9d-118">-InstanceName</span></span>
<span data-ttu-id="e0f9d-119">Az Azure SQL Felügyelt példány neve, amelybe csak az Azure Active Directory hitelesítés van beszúrva.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="e0f9d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0f9d-120">-ResourceGroupName</span></span>
<span data-ttu-id="e0f9d-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="e0f9d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0f9d-122">-ResourceId</span></span>
<span data-ttu-id="e0f9d-123">A használni használt példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e0f9d-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="e0f9d-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0f9d-124">-Confirm</span></span>
<span data-ttu-id="e0f9d-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0f9d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0f9d-126">-WhatIf</span></span>
<span data-ttu-id="e0f9d-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0f9d-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0f9d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0f9d-129">CommonParameters</span></span>
<span data-ttu-id="e0f9d-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0f9d-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0f9d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0f9d-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0f9d-132">INPUTS</span></span>

### <span data-ttu-id="e0f9d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e0f9d-133">System.String</span></span>

## <span data-ttu-id="e0f9d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0f9d-134">OUTPUTS</span></span>

### <span data-ttu-id="e0f9d-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="e0f9d-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="e0f9d-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e0f9d-136">NOTES</span></span>

## <span data-ttu-id="e0f9d-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0f9d-137">RELATED LINKS</span></span>

[<span data-ttu-id="e0f9d-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="e0f9d-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="e0f9d-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="e0f9d-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="e0f9d-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e0f9d-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="e0f9d-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e0f9d-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)