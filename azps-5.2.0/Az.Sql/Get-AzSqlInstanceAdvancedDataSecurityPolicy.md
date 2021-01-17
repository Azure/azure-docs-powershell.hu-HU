---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 8adb699375a1b53f20e6027f35772642c658928b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343193"
---
# <span data-ttu-id="c5186-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="c5186-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="c5186-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5186-102">SYNOPSIS</span></span>
<span data-ttu-id="c5186-103">Felügyelt példány speciális adatbiztonsági házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="c5186-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="c5186-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c5186-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5186-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c5186-105">DESCRIPTION</span></span>
<span data-ttu-id="c5186-106">A **Get-AzSqlInstanceAdvancedDataSecurityPolicy** parancsmag beolvassa egy felügyelt példány Speciális adatbiztonsági házirendet.</span><span class="sxs-lookup"><span data-stu-id="c5186-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="c5186-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c5186-107">EXAMPLES</span></span>

### <span data-ttu-id="c5186-108">1. példa: Felügyelt példány speciális adatbiztonságának lekérte</span><span class="sxs-lookup"><span data-stu-id="c5186-108">Example 1: Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="c5186-109">2. példa: Felügyelt példány speciális adatbiztonságát kapja a felügyelt példány erőforrástól</span><span class="sxs-lookup"><span data-stu-id="c5186-109">Example 2: Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="c5186-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5186-110">PARAMETERS</span></span>

### <span data-ttu-id="c5186-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5186-111">-DefaultProfile</span></span>
<span data-ttu-id="c5186-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5186-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5186-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5186-113">-InputObject</span></span>
<span data-ttu-id="c5186-114">The managed instance object to use with Advanced Data Security policy operation</span><span class="sxs-lookup"><span data-stu-id="c5186-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="c5186-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c5186-115">-InstanceName</span></span>
<span data-ttu-id="c5186-116">SQL-adatbázis felügyelt példány neve.</span><span class="sxs-lookup"><span data-stu-id="c5186-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="c5186-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5186-117">-ResourceGroupName</span></span>
<span data-ttu-id="c5186-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c5186-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="c5186-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5186-119">CommonParameters</span></span>
<span data-ttu-id="c5186-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5186-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5186-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5186-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5186-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5186-122">INPUTS</span></span>

### <span data-ttu-id="c5186-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="c5186-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="c5186-124">System.String</span><span class="sxs-lookup"><span data-stu-id="c5186-124">System.String</span></span>

## <span data-ttu-id="c5186-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5186-125">OUTPUTS</span></span>

### <span data-ttu-id="c5186-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c5186-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="c5186-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c5186-127">NOTES</span></span>

## <span data-ttu-id="c5186-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5186-128">RELATED LINKS</span></span>
