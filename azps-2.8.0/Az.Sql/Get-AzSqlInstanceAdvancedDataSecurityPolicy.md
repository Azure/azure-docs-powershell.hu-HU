---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 847fc240d9ac30613c78d2d703aef76fcbc1661f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839193"
---
# <span data-ttu-id="2dcca-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="2dcca-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="2dcca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2dcca-102">SYNOPSIS</span></span>
<span data-ttu-id="2dcca-103">A felügyelt példány speciális adatbiztonsági házirendjének lekérdezése.</span><span class="sxs-lookup"><span data-stu-id="2dcca-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="2dcca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2dcca-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2dcca-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2dcca-105">DESCRIPTION</span></span>
<span data-ttu-id="2dcca-106">A **Get-AzSqlInstanceAdvancedDataSecurityPolicy** parancsmag a felügyelt példány speciális adatbiztonsági házirendjének lekérdezését kéri.</span><span class="sxs-lookup"><span data-stu-id="2dcca-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="2dcca-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2dcca-107">EXAMPLES</span></span>

### <span data-ttu-id="2dcca-108">Példa 1 – a felügyelt példány speciális adatbiztonsága</span><span class="sxs-lookup"><span data-stu-id="2dcca-108">Example 1 - Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="2dcca-109">Példa: a felügyelt példány speciális adatbiztonsága a felügyelt példányok erőforrásból</span><span class="sxs-lookup"><span data-stu-id="2dcca-109">Example 2 - Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="2dcca-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2dcca-110">PARAMETERS</span></span>

### <span data-ttu-id="2dcca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dcca-111">-DefaultProfile</span></span>
<span data-ttu-id="2dcca-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2dcca-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dcca-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2dcca-113">-InputObject</span></span>
<span data-ttu-id="2dcca-114">A felügyelt instance objektum, amelyet a speciális adatbiztonsági házirend-művelethez használ</span><span class="sxs-lookup"><span data-stu-id="2dcca-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="2dcca-115">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="2dcca-115">-InstanceName</span></span>
<span data-ttu-id="2dcca-116">SQL-adatbázis felügyelt példányának neve.</span><span class="sxs-lookup"><span data-stu-id="2dcca-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="2dcca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dcca-117">-ResourceGroupName</span></span>
<span data-ttu-id="2dcca-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2dcca-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="2dcca-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dcca-119">CommonParameters</span></span>
<span data-ttu-id="2dcca-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2dcca-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dcca-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dcca-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dcca-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2dcca-122">INPUTS</span></span>

### <span data-ttu-id="2dcca-123">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="2dcca-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="2dcca-124">System. String</span><span class="sxs-lookup"><span data-stu-id="2dcca-124">System.String</span></span>

## <span data-ttu-id="2dcca-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2dcca-125">OUTPUTS</span></span>

### <span data-ttu-id="2dcca-126">Microsoft. Azure. Command. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="2dcca-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="2dcca-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2dcca-127">NOTES</span></span>

## <span data-ttu-id="2dcca-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2dcca-128">RELATED LINKS</span></span>
