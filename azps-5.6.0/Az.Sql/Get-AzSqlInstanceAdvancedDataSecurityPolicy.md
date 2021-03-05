---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 2d9fa7ef7d3763d2db1d963aa1b1cac41b711bd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014517"
---
# <span data-ttu-id="48476-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="48476-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="48476-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48476-102">SYNOPSIS</span></span>
<span data-ttu-id="48476-103">Felügyelt példány speciális adatbiztonsági házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="48476-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="48476-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="48476-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48476-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="48476-105">DESCRIPTION</span></span>
<span data-ttu-id="48476-106">A **Get-AzSqlInstanceAdvancedDataSecurityPolicy** parancsmag beolvassa egy felügyelt példány Speciális adatbiztonsági házirendet.</span><span class="sxs-lookup"><span data-stu-id="48476-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="48476-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="48476-107">EXAMPLES</span></span>

### <span data-ttu-id="48476-108">1. példa: Felügyelt példány speciális adatbiztonságának lekérte</span><span class="sxs-lookup"><span data-stu-id="48476-108">Example 1: Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="48476-109">2. példa: Felügyelt példány speciális adatbiztonságát kapja a felügyelt példány erőforrástól</span><span class="sxs-lookup"><span data-stu-id="48476-109">Example 2: Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="48476-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48476-110">PARAMETERS</span></span>

### <span data-ttu-id="48476-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48476-111">-DefaultProfile</span></span>
<span data-ttu-id="48476-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48476-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48476-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48476-113">-InputObject</span></span>
<span data-ttu-id="48476-114">The managed instance object to use with Advanced Data Security policy operation</span><span class="sxs-lookup"><span data-stu-id="48476-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="48476-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="48476-115">-InstanceName</span></span>
<span data-ttu-id="48476-116">SQL-adatbázis felügyelt példány neve.</span><span class="sxs-lookup"><span data-stu-id="48476-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="48476-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48476-117">-ResourceGroupName</span></span>
<span data-ttu-id="48476-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="48476-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="48476-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48476-119">CommonParameters</span></span>
<span data-ttu-id="48476-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48476-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48476-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48476-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48476-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="48476-122">INPUTS</span></span>

### <span data-ttu-id="48476-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="48476-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="48476-124">System.String</span><span class="sxs-lookup"><span data-stu-id="48476-124">System.String</span></span>

## <span data-ttu-id="48476-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48476-125">OUTPUTS</span></span>

### <span data-ttu-id="48476-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="48476-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="48476-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="48476-127">NOTES</span></span>

## <span data-ttu-id="48476-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48476-128">RELATED LINKS</span></span>
