---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: faf93387f068c6ee8e83653d31b96a1f3ecdef70
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669058"
---
# <span data-ttu-id="5d872-101">Enable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="5d872-101">Enable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="5d872-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d872-102">SYNOPSIS</span></span>
<span data-ttu-id="5d872-103">Lehetővé teszi a speciális adatbiztonságot egy felügyelt példányon.</span><span class="sxs-lookup"><span data-stu-id="5d872-103">Enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="5d872-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d872-104">SYNTAX</span></span>

```
Enable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d872-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d872-105">DESCRIPTION</span></span>
<span data-ttu-id="5d872-106">Az **enable-AzSqlInstanceAdvancedDataSecurity** parancsmag speciális adatbiztonságot engedélyez egy felügyelt példányon.</span><span class="sxs-lookup"><span data-stu-id="5d872-106">The **Enable-AzSqlInstanceAdvancedDataSecurity** cmdlet enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="5d872-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5d872-107">EXAMPLES</span></span>

### <span data-ttu-id="5d872-108">Példa 1 – a felügyelt példány speciális adatbiztonságának engedélyezése</span><span class="sxs-lookup"><span data-stu-id="5d872-108">Example 1 - Enable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" 

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="5d872-109">Példa 2 – a felügyelt példány speciális adatbiztonságának engedélyezése a kiszolgálói erőforrásból</span><span class="sxs-lookup"><span data-stu-id="5d872-109">Example 2 - Enable managed instance Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Enable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="5d872-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d872-110">PARAMETERS</span></span>

### <span data-ttu-id="5d872-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d872-111">-DefaultProfile</span></span>
<span data-ttu-id="5d872-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d872-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d872-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d872-113">-InputObject</span></span>
<span data-ttu-id="5d872-114">A felügyelt instance objektum, amelyet a speciális adatbiztonsági házirend-művelethez használ</span><span class="sxs-lookup"><span data-stu-id="5d872-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="5d872-115">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="5d872-115">-InstanceName</span></span>
<span data-ttu-id="5d872-116">SQL-adatbázis felügyelt példányának neve.</span><span class="sxs-lookup"><span data-stu-id="5d872-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="5d872-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d872-117">-ResourceGroupName</span></span>
<span data-ttu-id="5d872-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5d872-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="5d872-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5d872-119">-Confirm</span></span>
<span data-ttu-id="5d872-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5d872-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d872-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d872-121">-WhatIf</span></span>
<span data-ttu-id="5d872-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5d872-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d872-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5d872-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d872-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d872-124">CommonParameters</span></span>
<span data-ttu-id="5d872-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d872-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d872-126">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5d872-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d872-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d872-127">INPUTS</span></span>

### <span data-ttu-id="5d872-128">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="5d872-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="5d872-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5d872-129">System.String</span></span>

## <span data-ttu-id="5d872-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d872-130">OUTPUTS</span></span>

### <span data-ttu-id="5d872-131">Microsoft. Azure. Command. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5d872-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="5d872-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d872-132">NOTES</span></span>

## <span data-ttu-id="5d872-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d872-133">RELATED LINKS</span></span>
