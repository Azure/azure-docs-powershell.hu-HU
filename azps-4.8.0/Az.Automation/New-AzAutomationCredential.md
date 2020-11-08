---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
ms.openlocfilehash: a0b23cc5e16a723364d234eb2ee9723f291ee5e4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017937"
---
# <span data-ttu-id="3f95b-101">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3f95b-101">New-AzAutomationCredential</span></span>

## <span data-ttu-id="3f95b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f95b-102">SYNOPSIS</span></span>
<span data-ttu-id="3f95b-103">Automatizálási hitelesítő adatokat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3f95b-103">Creates an Automation credential.</span></span>

## <span data-ttu-id="3f95b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f95b-104">SYNTAX</span></span>

```
New-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f95b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f95b-105">DESCRIPTION</span></span>
<span data-ttu-id="3f95b-106">A **New-AzAutomationCredential** parancsmag **PSCredential** -objektumként hozza létre a hitelesítő adatait az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="3f95b-106">The **New-AzAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="3f95b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3f95b-107">EXAMPLES</span></span>

### <span data-ttu-id="3f95b-108">Példa 1: hitelesítő adatok létrehozása</span><span class="sxs-lookup"><span data-stu-id="3f95b-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3f95b-109">Az első parancs a felhasználónevet hozzárendeli a $User változóhoz.</span><span class="sxs-lookup"><span data-stu-id="3f95b-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="3f95b-110">A második parancs az egyszerű szöveges jelszót egy biztonságos karakterláncba konvertálja a ConvertTo-SecureString parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="3f95b-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="3f95b-111">A parancs az objektumot a $Password változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3f95b-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="3f95b-112">A harmadik parancs a hitelesítő adatokat $User és a $Password alapján hozza létre, majd a $Credential változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3f95b-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="3f95b-113">A végleges parancs létrehoz egy ContosoCredential nevű automatizálási hitelesítő adatokat, amely a $Credentialt használja.</span><span class="sxs-lookup"><span data-stu-id="3f95b-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="3f95b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f95b-114">PARAMETERS</span></span>

### <span data-ttu-id="3f95b-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3f95b-115">-AutomationAccountName</span></span>
<span data-ttu-id="3f95b-116">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag a hitelesítő adatokat tárolja.</span><span class="sxs-lookup"><span data-stu-id="3f95b-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f95b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f95b-117">-DefaultProfile</span></span>
<span data-ttu-id="3f95b-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3f95b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f95b-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="3f95b-119">-Description</span></span>
<span data-ttu-id="3f95b-120">A hitelesítő adatok leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f95b-120">Specifies a description for the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f95b-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3f95b-121">-Name</span></span>
<span data-ttu-id="3f95b-122">A hitelesítő adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f95b-122">Specifies a name for the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f95b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f95b-123">-ResourceGroupName</span></span>
<span data-ttu-id="3f95b-124">Annak az erőforráscsoportnak a leírását adja meg, amelyhez a parancsmag hitelesítő adatokat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3f95b-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="3f95b-125">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="3f95b-125">-Value</span></span>
<span data-ttu-id="3f95b-126">A hitelesítő adatokat **PSCredential** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f95b-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f95b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f95b-127">CommonParameters</span></span>
<span data-ttu-id="3f95b-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3f95b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f95b-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f95b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f95b-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f95b-130">INPUTS</span></span>

### <span data-ttu-id="3f95b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3f95b-131">System.String</span></span>

### <span data-ttu-id="3f95b-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="3f95b-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="3f95b-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f95b-133">OUTPUTS</span></span>

### <span data-ttu-id="3f95b-134">Microsoft. Azure. Command. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="3f95b-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="3f95b-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f95b-135">NOTES</span></span>

## <span data-ttu-id="3f95b-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f95b-136">RELATED LINKS</span></span>

[<span data-ttu-id="3f95b-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3f95b-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="3f95b-138">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3f95b-138">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="3f95b-139">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3f95b-139">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


