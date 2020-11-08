---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 599b4817ce9f4f6f1f7a75f5811c5a3122f1bbb7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183105"
---
# <span data-ttu-id="3a6cf-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="3a6cf-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="3a6cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a6cf-102">SYNOPSIS</span></span>
<span data-ttu-id="3a6cf-103">SQL Server-bővítmény eltávolítása virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="3a6cf-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="3a6cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a6cf-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a6cf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a6cf-105">DESCRIPTION</span></span>
<span data-ttu-id="3a6cf-106">A **Remove-AzVMSqlServerExtension** parancsmag eltávolítja a AzureSQL Server-bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="3a6cf-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="3a6cf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3a6cf-107">EXAMPLES</span></span>

### <span data-ttu-id="3a6cf-108">1. példa: SQL Server-bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3a6cf-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="3a6cf-109">Ez a parancs eltávolítja az SQL Server-bővítményt a ContosoVM22 nevű virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="3a6cf-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="3a6cf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a6cf-110">PARAMETERS</span></span>

### <span data-ttu-id="3a6cf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a6cf-111">-DefaultProfile</span></span>
<span data-ttu-id="3a6cf-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a6cf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a6cf-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3a6cf-113">-Name</span></span>
<span data-ttu-id="3a6cf-114">Annak az SQL-kiszolgálónak a neve, amely a parancsmag által eltávolított bővítmény.</span><span class="sxs-lookup"><span data-stu-id="3a6cf-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a6cf-115">-Várva</span><span class="sxs-lookup"><span data-stu-id="3a6cf-115">-NoWait</span></span>
<span data-ttu-id="3a6cf-116">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="3a6cf-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="3a6cf-117">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="3a6cf-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="3a6cf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a6cf-118">-ResourceGroupName</span></span>
<span data-ttu-id="3a6cf-119">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a6cf-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3a6cf-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="3a6cf-120">-VMName</span></span>
<span data-ttu-id="3a6cf-121">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja az SQL Server-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="3a6cf-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a6cf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a6cf-122">CommonParameters</span></span>
<span data-ttu-id="3a6cf-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a6cf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a6cf-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3a6cf-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a6cf-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a6cf-125">INPUTS</span></span>

### <span data-ttu-id="3a6cf-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3a6cf-126">System.String</span></span>

## <span data-ttu-id="3a6cf-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a6cf-127">OUTPUTS</span></span>

### <span data-ttu-id="3a6cf-128">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3a6cf-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3a6cf-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a6cf-129">NOTES</span></span>

## <span data-ttu-id="3a6cf-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a6cf-130">RELATED LINKS</span></span>

[<span data-ttu-id="3a6cf-131">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="3a6cf-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="3a6cf-132">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="3a6cf-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


