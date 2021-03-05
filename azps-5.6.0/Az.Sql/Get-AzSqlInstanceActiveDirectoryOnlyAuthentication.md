---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 0a06eae51b074cefb74b2ef3a175a056cc52ff84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014549"
---
# <span data-ttu-id="f856a-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="f856a-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="f856a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f856a-102">SYNOPSIS</span></span>
<span data-ttu-id="f856a-103">Az Azure AD-hitelesítést csak egy adott SQL Felügyelt példány esetén kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f856a-103">Gets Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="f856a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f856a-104">SYNTAX</span></span>

### <span data-ttu-id="f856a-105">UseResourceGroupAndInstanceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f856a-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f856a-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f856a-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f856a-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f856a-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f856a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f856a-108">DESCRIPTION</span></span>
<span data-ttu-id="f856a-109">A **Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** parancsmag csak az Azure Active Directory (Azure AD) hitelesítéskövetelményét kapja meg az aktuális előfizetésben lévő AzureSQL Felügyelt példányhoz.</span><span class="sxs-lookup"><span data-stu-id="f856a-109">The **Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="f856a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f856a-110">EXAMPLES</span></span>

### <span data-ttu-id="f856a-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="f856a-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
```

<span data-ttu-id="f856a-112">Ez a parancs csak az Azure Active Directory (Azure AD) hitelesítését követeli meg egy ManagedInstance01 nevű Felügyelt Példány nevű AzureSQL-hez, amely egy ResourceGroup01 nevű erőforráscsoporthoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="f856a-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="f856a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f856a-113">PARAMETERS</span></span>

### <span data-ttu-id="f856a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f856a-114">-DefaultProfile</span></span>
<span data-ttu-id="f856a-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f856a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f856a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f856a-116">-InputObject</span></span>
<span data-ttu-id="f856a-117">A használni használt felügyeltpéldány-objektum.</span><span class="sxs-lookup"><span data-stu-id="f856a-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="f856a-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="f856a-118">-InstanceName</span></span>
<span data-ttu-id="f856a-119">Az Azure SQL Felügyelt példány neve, amelybe csak az Azure Active Directory hitelesítés van beszúrva.</span><span class="sxs-lookup"><span data-stu-id="f856a-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="f856a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f856a-120">-ResourceGroupName</span></span>
<span data-ttu-id="f856a-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f856a-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="f856a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f856a-122">-ResourceId</span></span>
<span data-ttu-id="f856a-123">A használni használt példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f856a-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="f856a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f856a-124">-Confirm</span></span>
<span data-ttu-id="f856a-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f856a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f856a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f856a-126">-WhatIf</span></span>
<span data-ttu-id="f856a-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f856a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f856a-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f856a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f856a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f856a-129">CommonParameters</span></span>
<span data-ttu-id="f856a-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f856a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f856a-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f856a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f856a-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f856a-132">INPUTS</span></span>

### <span data-ttu-id="f856a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f856a-133">System.String</span></span>

## <span data-ttu-id="f856a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f856a-134">OUTPUTS</span></span>

### <span data-ttu-id="f856a-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="f856a-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="f856a-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f856a-136">NOTES</span></span>

## <span data-ttu-id="f856a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f856a-137">RELATED LINKS</span></span>

[<span data-ttu-id="f856a-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="f856a-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="f856a-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="f856a-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="f856a-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f856a-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="f856a-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f856a-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

