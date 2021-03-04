---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 4116ddf22bb39ddfa78e07180aaf61da7e87bb7f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933689"
---
# <span data-ttu-id="c0344-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="c0344-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="c0344-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0344-102">SYNOPSIS</span></span>
<span data-ttu-id="c0344-103">Letiltja a speciális adatbiztonságot egy felügyelt példányon.</span><span class="sxs-lookup"><span data-stu-id="c0344-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="c0344-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c0344-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0344-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c0344-105">DESCRIPTION</span></span>
<span data-ttu-id="c0344-106">A **Disable-AzSqlInstanceAdvancedDataSecurity** parancsmag letiltja a speciális adatbiztonságot egy felügyelt példányon.</span><span class="sxs-lookup"><span data-stu-id="c0344-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="c0344-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c0344-107">EXAMPLES</span></span>

### <span data-ttu-id="c0344-108">1. példa: A felügyelt példány speciális adatbiztonságának letiltása</span><span class="sxs-lookup"><span data-stu-id="c0344-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="c0344-109">2. példa: A kiszolgáló speciális adatbiztonságának letiltása felügyelt példány típusú erőforrásból</span><span class="sxs-lookup"><span data-stu-id="c0344-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="c0344-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0344-110">PARAMETERS</span></span>

### <span data-ttu-id="c0344-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0344-111">-DefaultProfile</span></span>
<span data-ttu-id="c0344-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0344-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0344-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0344-113">-InputObject</span></span>
<span data-ttu-id="c0344-114">The managed instance object to use with Advanced Data Security policy operation</span><span class="sxs-lookup"><span data-stu-id="c0344-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0344-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c0344-115">-InstanceName</span></span>
<span data-ttu-id="c0344-116">SQL-adatbázis felügyelt példány neve.</span><span class="sxs-lookup"><span data-stu-id="c0344-116">SQL Database managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0344-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0344-117">-ResourceGroupName</span></span>
<span data-ttu-id="c0344-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c0344-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="c0344-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0344-119">-Confirm</span></span>
<span data-ttu-id="c0344-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c0344-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0344-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0344-121">-WhatIf</span></span>
<span data-ttu-id="c0344-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c0344-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0344-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c0344-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0344-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0344-124">CommonParameters</span></span>
<span data-ttu-id="c0344-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0344-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0344-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0344-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0344-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0344-127">INPUTS</span></span>

### <span data-ttu-id="c0344-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="c0344-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="c0344-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c0344-129">System.String</span></span>

## <span data-ttu-id="c0344-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0344-130">OUTPUTS</span></span>

### <span data-ttu-id="c0344-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c0344-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="c0344-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c0344-132">NOTES</span></span>

## <span data-ttu-id="c0344-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0344-133">RELATED LINKS</span></span>
