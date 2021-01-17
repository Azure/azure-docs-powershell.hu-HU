---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
ms.openlocfilehash: e44b9a5c497aba5533d53acdc9aab31cb5ece703
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478501"
---
# <span data-ttu-id="9c3e0-101">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9c3e0-101">Set-AzAutomationCredential</span></span>

## <span data-ttu-id="9c3e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c3e0-102">SYNOPSIS</span></span>
<span data-ttu-id="9c3e0-103">Módosítja az automatizálási hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="9c3e0-103">Modifies an Automation credential.</span></span>

## <span data-ttu-id="9c3e0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9c3e0-104">SYNTAX</span></span>

```
Set-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c3e0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9c3e0-105">DESCRIPTION</span></span>
<span data-ttu-id="9c3e0-106">A **Set-AzAutomationCredential** parancsmag módosítja a hitelesítő adatokat **PSCredential** objektumként az Azure Automationben.</span><span class="sxs-lookup"><span data-stu-id="9c3e0-106">The **Set-AzAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="9c3e0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9c3e0-107">EXAMPLES</span></span>

### <span data-ttu-id="9c3e0-108">1. példa: Hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="9c3e0-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="9c3e0-109">Az első parancs hozzárendel egy felhasználónevet a $User változóhoz.</span><span class="sxs-lookup"><span data-stu-id="9c3e0-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="9c3e0-110">A második parancs egy egyszerű szöveges jelszót biztonságos karakterláncsá alakít át a ConvertTo-SecureString parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="9c3e0-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="9c3e0-111">A parancs az objektumot a $Password tárolja.</span><span class="sxs-lookup"><span data-stu-id="9c3e0-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="9c3e0-112">A harmadik parancs létrehoz egy hitelesítő adatokat a $User és $Password alapján, majd tárolja azt a $Credential változóban.</span><span class="sxs-lookup"><span data-stu-id="9c3e0-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="9c3e0-113">Az utolsó parancs módosítja a ContosoCredential nevű automatizálási hitelesítő adatokat a hitelesítő adatok $Credential.</span><span class="sxs-lookup"><span data-stu-id="9c3e0-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="9c3e0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c3e0-114">PARAMETERS</span></span>

### <span data-ttu-id="9c3e0-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9c3e0-115">-AutomationAccountName</span></span>
<span data-ttu-id="9c3e0-116">Annak az automatizálási fióknak a nevét adja meg, amelynek a parancsmagja módosítja a hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="9c3e0-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="9c3e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c3e0-117">-DefaultProfile</span></span>
<span data-ttu-id="9c3e0-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9c3e0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c3e0-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="9c3e0-119">-Description</span></span>
<span data-ttu-id="9c3e0-120">Megadja annak a hitelesítő adatnak a leírását, amit ez a parancsmag módosít.</span><span class="sxs-lookup"><span data-stu-id="9c3e0-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9c3e0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9c3e0-121">-Name</span></span>
<span data-ttu-id="9c3e0-122">Megadja annak a hitelesítő adatnak a nevét, amit ez a parancsmag módosít.</span><span class="sxs-lookup"><span data-stu-id="9c3e0-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9c3e0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c3e0-123">-ResourceGroupName</span></span>
<span data-ttu-id="9c3e0-124">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja módosítja a hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="9c3e0-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="9c3e0-125">-Érték</span><span class="sxs-lookup"><span data-stu-id="9c3e0-125">-Value</span></span>
<span data-ttu-id="9c3e0-126">A hitelesítő adatokat **PSCredential** objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c3e0-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c3e0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c3e0-127">CommonParameters</span></span>
<span data-ttu-id="9c3e0-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c3e0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c3e0-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c3e0-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c3e0-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c3e0-130">INPUTS</span></span>

### <span data-ttu-id="9c3e0-131">System.String</span><span class="sxs-lookup"><span data-stu-id="9c3e0-131">System.String</span></span>

### <span data-ttu-id="9c3e0-132">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="9c3e0-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="9c3e0-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c3e0-133">OUTPUTS</span></span>

### <span data-ttu-id="9c3e0-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="9c3e0-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="9c3e0-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9c3e0-135">NOTES</span></span>

## <span data-ttu-id="9c3e0-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c3e0-136">RELATED LINKS</span></span>

[<span data-ttu-id="9c3e0-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9c3e0-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="9c3e0-138">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9c3e0-138">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="9c3e0-139">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9c3e0-139">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)


