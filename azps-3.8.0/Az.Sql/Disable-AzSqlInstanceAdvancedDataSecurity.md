---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 39b23c1b39121f143791667ade542080ba70ec95
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846641"
---
# <span data-ttu-id="7a7a2-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="7a7a2-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="7a7a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7a7a2-102">SYNOPSIS</span></span>
<span data-ttu-id="7a7a2-103">A továbbfejlesztett adatbiztonság letiltása egy felügyelt példányon.</span><span class="sxs-lookup"><span data-stu-id="7a7a2-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="7a7a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7a7a2-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a7a2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7a7a2-105">DESCRIPTION</span></span>
<span data-ttu-id="7a7a2-106">A **disable-AzSqlInstanceAdvancedDataSecurity** parancsmag a továbbfejlesztett adatbiztonságot letiltja egy felügyelt példányon.</span><span class="sxs-lookup"><span data-stu-id="7a7a2-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="7a7a2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7a7a2-107">EXAMPLES</span></span>

### <span data-ttu-id="7a7a2-108">Példa 1 – a felügyelt példány speciális adatbiztonságának letiltása</span><span class="sxs-lookup"><span data-stu-id="7a7a2-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="7a7a2-109">Példa 2 – a kiszolgáló speciális adatbiztonságának letiltása a felügyelt példányok erőforrásból</span><span class="sxs-lookup"><span data-stu-id="7a7a2-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="7a7a2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7a7a2-110">PARAMETERS</span></span>

### <span data-ttu-id="7a7a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a7a2-111">-DefaultProfile</span></span>
<span data-ttu-id="7a7a2-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a7a2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a7a2-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a7a2-113">-InputObject</span></span>
<span data-ttu-id="7a7a2-114">A felügyelt instance objektum, amelyet a speciális adatbiztonsági házirend-művelethez használ</span><span class="sxs-lookup"><span data-stu-id="7a7a2-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="7a7a2-115">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="7a7a2-115">-InstanceName</span></span>
<span data-ttu-id="7a7a2-116">SQL-adatbázis felügyelt példányának neve.</span><span class="sxs-lookup"><span data-stu-id="7a7a2-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="7a7a2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a7a2-117">-ResourceGroupName</span></span>
<span data-ttu-id="7a7a2-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7a7a2-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="7a7a2-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7a7a2-119">-Confirm</span></span>
<span data-ttu-id="7a7a2-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7a7a2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a7a2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a7a2-121">-WhatIf</span></span>
<span data-ttu-id="7a7a2-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7a7a2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a7a2-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7a7a2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a7a2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a7a2-124">CommonParameters</span></span>
<span data-ttu-id="7a7a2-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7a7a2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a7a2-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7a7a2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a7a2-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a7a2-127">INPUTS</span></span>

### <span data-ttu-id="7a7a2-128">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="7a7a2-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="7a7a2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7a7a2-129">System.String</span></span>

## <span data-ttu-id="7a7a2-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a7a2-130">OUTPUTS</span></span>

### <span data-ttu-id="7a7a2-131">Microsoft. Azure. Command. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="7a7a2-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="7a7a2-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7a7a2-132">NOTES</span></span>

## <span data-ttu-id="7a7a2-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a7a2-133">RELATED LINKS</span></span>
