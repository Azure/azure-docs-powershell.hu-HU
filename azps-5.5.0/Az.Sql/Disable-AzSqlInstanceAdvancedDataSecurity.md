---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 39b23c1b39121f143791667ade542080ba70ec95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163434"
---
# <span data-ttu-id="87b62-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="87b62-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="87b62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87b62-102">SYNOPSIS</span></span>
<span data-ttu-id="87b62-103">Letiltja a speciális adatbiztonságot egy felügyelt példányon.</span><span class="sxs-lookup"><span data-stu-id="87b62-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="87b62-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="87b62-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87b62-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="87b62-105">DESCRIPTION</span></span>
<span data-ttu-id="87b62-106">A **Disable-AzSqlInstanceAdvancedDataSecurity** parancsmag letiltja a speciális adatbiztonságot egy felügyelt példányon.</span><span class="sxs-lookup"><span data-stu-id="87b62-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="87b62-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="87b62-107">EXAMPLES</span></span>

### <span data-ttu-id="87b62-108">1. példa: A felügyelt példány speciális adatbiztonságának letiltása</span><span class="sxs-lookup"><span data-stu-id="87b62-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="87b62-109">2. példa: A kiszolgáló speciális adatbiztonságának letiltása felügyelt példány típusú erőforrásból</span><span class="sxs-lookup"><span data-stu-id="87b62-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="87b62-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87b62-110">PARAMETERS</span></span>

### <span data-ttu-id="87b62-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87b62-111">-DefaultProfile</span></span>
<span data-ttu-id="87b62-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87b62-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87b62-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87b62-113">-InputObject</span></span>
<span data-ttu-id="87b62-114">The managed instance object to use with Advanced Data Security policy operation</span><span class="sxs-lookup"><span data-stu-id="87b62-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="87b62-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="87b62-115">-InstanceName</span></span>
<span data-ttu-id="87b62-116">SQL-adatbázis felügyelt példány neve.</span><span class="sxs-lookup"><span data-stu-id="87b62-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="87b62-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87b62-117">-ResourceGroupName</span></span>
<span data-ttu-id="87b62-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="87b62-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="87b62-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87b62-119">-Confirm</span></span>
<span data-ttu-id="87b62-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="87b62-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87b62-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87b62-121">-WhatIf</span></span>
<span data-ttu-id="87b62-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="87b62-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87b62-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="87b62-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87b62-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87b62-124">CommonParameters</span></span>
<span data-ttu-id="87b62-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87b62-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87b62-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87b62-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87b62-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87b62-127">INPUTS</span></span>

### <span data-ttu-id="87b62-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="87b62-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="87b62-129">System.String</span><span class="sxs-lookup"><span data-stu-id="87b62-129">System.String</span></span>

## <span data-ttu-id="87b62-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87b62-130">OUTPUTS</span></span>

### <span data-ttu-id="87b62-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="87b62-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="87b62-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="87b62-132">NOTES</span></span>

## <span data-ttu-id="87b62-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87b62-133">RELATED LINKS</span></span>
