---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 981baf0b0cd4d3ca70d18ab43b08bb2a16f7708f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846774"
---
# <span data-ttu-id="fb0cf-101">Enable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="fb0cf-101">Enable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="fb0cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb0cf-102">SYNOPSIS</span></span>
<span data-ttu-id="fb0cf-103">Lehetővé teszi a speciális adatbiztonságot egy felügyelt példányon.</span><span class="sxs-lookup"><span data-stu-id="fb0cf-103">Enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="fb0cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb0cf-104">SYNTAX</span></span>

```
Enable-AzSqlInstanceAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb0cf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb0cf-105">DESCRIPTION</span></span>
<span data-ttu-id="fb0cf-106">Az **enable-AzSqlInstanceAdvancedDataSecurity** parancsmag speciális adatbiztonságot engedélyez egy felügyelt példányon.</span><span class="sxs-lookup"><span data-stu-id="fb0cf-106">The **Enable-AzSqlInstanceAdvancedDataSecurity** cmdlet enables Advanced Data Security on a managed instance.</span></span> <span data-ttu-id="fb0cf-107">A speciális adatbiztonság egy olyan egységes biztonsági csomag, amely az adatosztályozást, a sebezhetőségi felmérést és a speciális veszélyforrások védelmét tartalmazza a felügyelt példányban.</span><span class="sxs-lookup"><span data-stu-id="fb0cf-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your managed instance.</span></span> <span data-ttu-id="fb0cf-108">(Új tárolási fiókot hoz létre a program automatikusan a sebezhetőségi felmérések mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="fb0cf-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="fb0cf-109">Ha korábban már létrehozott egy tárolási fiókot erre a célra, akkor a program Ehelyett ezt fogja használni.</span><span class="sxs-lookup"><span data-stu-id="fb0cf-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="fb0cf-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fb0cf-110">EXAMPLES</span></span>

### <span data-ttu-id="fb0cf-111">Példa 1 – a felügyelt példány speciális adatbiztonságának engedélyezése</span><span class="sxs-lookup"><span data-stu-id="fb0cf-111">Example 1 - Enable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" 

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="fb0cf-112">Példa 2 – a felügyelt példány speciális adatbiztonságának engedélyezése a kiszolgálói erőforrásból</span><span class="sxs-lookup"><span data-stu-id="fb0cf-112">Example 2 - Enable managed instance Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Enable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="fb0cf-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb0cf-113">PARAMETERS</span></span>

### <span data-ttu-id="fb0cf-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb0cf-114">-AsJob</span></span>
<span data-ttu-id="fb0cf-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fb0cf-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb0cf-116">-DefaultProfile</span></span>
<span data-ttu-id="fb0cf-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb0cf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb0cf-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="fb0cf-118">-DeploymentName</span></span>
<span data-ttu-id="fb0cf-119">Adjon meg egy egyéni nevet a speciális adatbiztonság telepítéséhez</span><span class="sxs-lookup"><span data-stu-id="fb0cf-119">Supply a custom name for Advanced Data Security deployment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0cf-120">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="fb0cf-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="fb0cf-121">Ne engedélyezze az automatikus biztonsági rések felmérését (ez nem hoz létre tárolási fiókot)</span><span class="sxs-lookup"><span data-stu-id="fb0cf-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0cf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb0cf-122">-InputObject</span></span>
<span data-ttu-id="fb0cf-123">A felügyelt instance objektum, amelyet a speciális adatbiztonsági házirend-művelethez használ</span><span class="sxs-lookup"><span data-stu-id="fb0cf-123">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="fb0cf-124">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="fb0cf-124">-InstanceName</span></span>
<span data-ttu-id="fb0cf-125">SQL-adatbázis felügyelt példányának neve.</span><span class="sxs-lookup"><span data-stu-id="fb0cf-125">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="fb0cf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb0cf-126">-ResourceGroupName</span></span>
<span data-ttu-id="fb0cf-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fb0cf-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="fb0cf-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fb0cf-128">-Confirm</span></span>
<span data-ttu-id="fb0cf-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fb0cf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb0cf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb0cf-130">-WhatIf</span></span>
<span data-ttu-id="fb0cf-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fb0cf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb0cf-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb0cf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb0cf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb0cf-133">CommonParameters</span></span>
<span data-ttu-id="fb0cf-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb0cf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb0cf-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fb0cf-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb0cf-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb0cf-136">INPUTS</span></span>

### <span data-ttu-id="fb0cf-137">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="fb0cf-137">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="fb0cf-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fb0cf-138">System.String</span></span>

## <span data-ttu-id="fb0cf-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb0cf-139">OUTPUTS</span></span>

### <span data-ttu-id="fb0cf-140">Microsoft. Azure. Command. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="fb0cf-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="fb0cf-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb0cf-141">NOTES</span></span>

## <span data-ttu-id="fb0cf-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb0cf-142">RELATED LINKS</span></span>
