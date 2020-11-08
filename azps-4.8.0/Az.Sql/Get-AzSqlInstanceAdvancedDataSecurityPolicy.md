---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 8adb699375a1b53f20e6027f35772642c658928b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183257"
---
# <span data-ttu-id="412d3-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="412d3-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="412d3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="412d3-102">SYNOPSIS</span></span>
<span data-ttu-id="412d3-103">A felügyelt példány speciális adatbiztonsági házirendjének lekérdezése.</span><span class="sxs-lookup"><span data-stu-id="412d3-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="412d3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="412d3-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="412d3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="412d3-105">DESCRIPTION</span></span>
<span data-ttu-id="412d3-106">A **Get-AzSqlInstanceAdvancedDataSecurityPolicy** parancsmag a felügyelt példány speciális adatbiztonsági házirendjének lekérdezését kéri.</span><span class="sxs-lookup"><span data-stu-id="412d3-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="412d3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="412d3-107">EXAMPLES</span></span>

### <span data-ttu-id="412d3-108">1. példa: a felügyelt példány speciális adatbiztonsága</span><span class="sxs-lookup"><span data-stu-id="412d3-108">Example 1: Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="412d3-109">2. példa: a felügyelt példány speciális adatbiztonsága a felügyelt példányok erőforrásból</span><span class="sxs-lookup"><span data-stu-id="412d3-109">Example 2: Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="412d3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="412d3-110">PARAMETERS</span></span>

### <span data-ttu-id="412d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="412d3-111">-DefaultProfile</span></span>
<span data-ttu-id="412d3-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="412d3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="412d3-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="412d3-113">-InputObject</span></span>
<span data-ttu-id="412d3-114">A felügyelt instance objektum, amelyet a speciális adatbiztonsági házirend-művelethez használ</span><span class="sxs-lookup"><span data-stu-id="412d3-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="412d3-115">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="412d3-115">-InstanceName</span></span>
<span data-ttu-id="412d3-116">SQL-adatbázis felügyelt példányának neve.</span><span class="sxs-lookup"><span data-stu-id="412d3-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="412d3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="412d3-117">-ResourceGroupName</span></span>
<span data-ttu-id="412d3-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="412d3-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="412d3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="412d3-119">CommonParameters</span></span>
<span data-ttu-id="412d3-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="412d3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="412d3-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="412d3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="412d3-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="412d3-122">INPUTS</span></span>

### <span data-ttu-id="412d3-123">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="412d3-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="412d3-124">System. String</span><span class="sxs-lookup"><span data-stu-id="412d3-124">System.String</span></span>

## <span data-ttu-id="412d3-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="412d3-125">OUTPUTS</span></span>

### <span data-ttu-id="412d3-126">Microsoft. Azure. Command. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="412d3-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="412d3-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="412d3-127">NOTES</span></span>

## <span data-ttu-id="412d3-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="412d3-128">RELATED LINKS</span></span>
